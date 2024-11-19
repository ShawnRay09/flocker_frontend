---
permalink: /voteforthegoat/calicovote/house
menu: nav/vote_for_the_goat.html
layout: post
title: Entering The House
Authors: Maryam, Nora, Kushi, Joanna
---
<script type="module" src="{{site.baseurl}}/navigation/voteforthegoat/calico.js"></script>

<style>
    /* Base Styles */
    body {
        font-family: "Times New Roman", Times, serif;
        transition: background-color 0.5s ease;
        color: #fff;
        margin: 0;
        padding: 0;
        min-height: 100vh;
        display: flex; 
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    /* Content Container */
    .content {
        padding: 20px;
        max-width: 600px;
        margin: 20px;
        border-radius: 10px;
        text-align: center;
        background: rgba(0, 0, 0, 0.5);
    }
    /* House Information */
    .house-info {
        font-size: 28px;
        font-weight: bold;
        margin-bottom: 15px;
    }
    .message {
        font-size: 20px;
        margin-bottom: 20px;
    }
    /* Button Styles */
    .button {
        padding: 10px 20px;
        font-size: 18px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        background-color: rgba(255, 255, 255, 0.2);
        color: #fff;
        transition: background-color 0.3s ease;
        margin-bottom: 10px;
    }
    .button:hover {
        background-color: rgba(255, 255, 255, 0.4);
    }
    /* Post Container */
    .post-container {
        background: rgba(255, 255, 255, 0.2);
        padding: 15px;
        margin: 10px auto;
        border-radius: 10px;
        text-align: left;
        width: 80%;
        max-width: 400px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    .post-button {
        padding: 8px 15px;
        margin-top: 10px;
        cursor: pointer;
        border-radius: 5px;
        border: none;
        background-color: #444;
        color: #fff;
    }
    .post-button:hover {
        background-color: #666;
    }
    .textarea-container {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    textarea {
        width: 90%;
        max-width: 380px;
        height: 100px;
        border-radius: 8px;
        padding: 10px;
        border: 1px solid #ddd;
        margin-bottom: 10px;
    }
    .image-preview {
        max-width: 100%;
        border-radius: 8px;
        margin-top: 10px;
    }
.cute-link {
    color: #ff69b4; 
    text-decoration: none;
    transition: all 0.1s ease-in-out;
}

.cute-link:hover {
    color: #ff1493;
    text-shadow: 0 0 8px rgba(255, 105, 180, 0.8), 
    0 0 15px rgba(255, 20, 147, 0.6), 
    0 0 20px rgba(255, 20, 147, 0.5);
}
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f9f9f9;
    color: #333;
    margin: 0;
}

.sidebar {
    position: fixed;
    top: 0;
    right: 75px;
    height: 500px;
    width: 150px;
    background-color: #fff;
    border: 1px solid #ddd;
    box-shadow: -2px 0 5px rgba(0, 0, 0, 0.1);
    border-radius: 20px; 
    padding-top: 20px;
    margin-top: 150px; 
    overflow-y: auto;
    overflow-x: hidden;
}

.sidebar-button {
    display: block;
    padding: 10px 20px;
    text-decoration: none;
    color: #333;
    font-weight: bold;
    transition: background-color 0.3s, color 0.3s;
}

.sidebar-button:hover {
    background-color: #ffb6c1;
    color: #fff;
}
.sidebar::-webkit-scrollbar-thumb {
    background-color: transparent;
    }
</style>

 <div class="sidebar">
        <button class="sidebar-button" data-house="Adventure Play House" data-channel-id="22" id="adventure-play-house">Adventure Play House</button>
        <button class="sidebar-button" data-house="Sylvanian Family Restraunt House" data-channel-id="23" id="sylvanian-restaurant-house">Sylvanian Family Restraunt House</button>
        <button class="sidebar-button" data-house="Magical Mermaid Castle House" data-channel-id="24" id="magical-mermaid-castle">Magical Mermaid Castle House</button>
        <button class="sidebar-button" data-house="Woody School House" data-channel-id="25" id="woody-school">Woody School House</button>
        <button class="sidebar-button" data-house="Spooky Suprise Haunted House" data-channel-id="26" id="spooky-surprise-haunted">Spooky Suprise Haunted House</button>
        <button class="sidebar-button" data-house="Brick Oven Bakery House" data-channel-id="27" id="brick-oven-bakery">Brick Oven Bakery House</button>
    </div>

<div class="content">
    <div id="houseInfo" class="house-info">Loading...</div>
    <div id="message" class="message">Please wait...</div>
    <button id="addPostButton" class="button">Add Post</button>
    <button id="backButton" class="button">Go Back</button>
    <button id="clearPostsButton">Clear All Posts</button>
    <div id="postsContainer"></div>
</div>

<div class="container">
    <div class="form-container">
        <form id="selectionForm">
            <input type="hidden" id="group_id" name="group_id" value="Calico Vote">
            <label for="channel_id">Channel:</label>
            <select id="channel_id" name="channel_id" required>
                <option value="">Select a channel</option>
                <option value="" data-channel-id="22">Adventure Play House</option>
                <option value="" data-channel-id="23">Sylvanian Family Restraunt House</option>
                <option value="" data-channel-id="24">Magical Mermaid Castle House</option>
                <option value="" data-channel-id="25">Woody School House</option>
                <option value="" data-channel-id="26">Spooky Suprise Haunted House</option>
                <option value="" data-channel-id="27">Brick Oven Bakery House</option>
            </select>
            <button type="submit">Select</button>
        </form>
    </div>
</div>



<script>
        const groupId = "Calico Vote";
        window.onload = function() {
        const savedHouse = localStorage.getItem('selectedHouse');
        const houseInfo = document.getElementById('houseInfo');
        const message = document.getElementById('message');
        const pageTitle = document.getElementById('pageTitle');
        console.log(`Stored house value: ${savedHouse}`);
        if (savedHouse) {
            console.log(`Setting background color and content for ${savedHouse}`);
            setBackground(savedHouse);
            renderHousePage(savedHouse);
            houseInfo.textContent = `You selected: ${savedHouse} House`;
            // Update page title and description based on the house
            pageTitle.textContent = `${savedHouse} House Page`;
            document.querySelector('meta[name="description"]').setAttribute('content', `Explore the ${savedHouse} House and its activities.`);
        } else {
            houseInfo.textContent = "No house selected.";
            message.textContent = "Please go back and select a house.";
        }
        fetchChannels(); // Fetch and populate channels dynamically
        displayPosts(savedHouse);
    };
    function setBackground(house) {
    let color;
    switch (house) {
        case 'Adventure Play':
            color = 'goldenrod';
            break;
        case 'Sylvanian Family Restaurant':
            color = 'blue';
            break;
        case 'Magical Mermaid Castle':
            color = 'purple';
            break;
        case 'Woody School':
            color = 'green';
            break;
        case 'Spooky Surprise Haunted':
            color = 'red';
            break;
        case 'Brick Oven Bakery':
            color = 'orange';
            break;
        default:
            color = 'black';
    }
    document.body.style.cssText = `background: ${color} !important; transition: background-color 0.5s ease;`;
}
    function renderHousePage(house) {
        const houseInfo = document.getElementById('houseInfo');
        const message = document.getElementById('message');
        switch (house) {
            case 'Adventure Play':
                houseInfo.textContent = "Welcome to the Adventure Play House!";
                message.textContent = "Explore and have fun!";
                break;
            case 'Sylvanian Family Restaurant':
                houseInfo.textContent = "Welcome to the Sylvanian Family Restaurant House!";
                message.textContent = "Join us for a delightful meal!";
                break;
            case 'Magical Mermaid Castle':
                houseInfo.textContent = "Welcome to the Magical Mermaid Castle!";
                message.textContent = "Dive into an enchanting experience!";
                break;
            case 'Woody School':
                houseInfo.textContent = "Welcome to the Woody School House!";
                message.textContent = "Get ready to learn and grow!";
                break;
            case 'Spooky Surprise Haunted':
                houseInfo.textContent = "Welcome to the Spooky Surprise Haunted House!";
                message.textContent = "Dare to enter the haunted halls!";
                break;
            case 'Brick Oven Bakery':
                houseInfo.textContent = "Welcome to the Brick Oven Bakery House!";
                message.textContent = "Smell the freshly baked goodies!";
                break;
            default:
                houseInfo.textContent = "House not found.";
                message.textContent = "Please go back and select a house.";
        }
    }
    function goBack() {
        window.history.back();
    }
    document.getElementById('backButton').addEventListener('click', goBack);
    document.getElementById('addPostButton').addEventListener('click', function() {
        const savedHouse = localStorage.getItem('selectedHouse');
        if (!savedHouse) {
            alert('Please select a house first!');
            return;
        }
        const postContainer = document.createElement('div');
        postContainer.classList.add('post-container');
        const textArea = document.createElement('textarea');
        const imageInput = document.createElement('input');
        imageInput.type = 'file';
        imageInput.accept = 'image/*';
        const imagePreview = document.createElement('img');
        imagePreview.classList.add('image-preview');
        imageInput.onchange = function() {
            const file = imageInput.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    imagePreview.src = e.target.result;
                    imagePreview.style.display = 'block';
                };
                reader.readAsDataURL(file);
            }
        };
        const postButton = document.createElement('button');
        postButton.textContent = 'Post';
        postButton.classList.add('post-button');
        postButton.onclick = function() {
            savePost(savedHouse, textArea.value, imagePreview.src);
            displayPosts(savedHouse);
            postContainer.remove();
        };
        postContainer.appendChild(textArea);
        postContainer.appendChild(imageInput);
        postContainer.appendChild(imagePreview);
        postContainer.appendChild(postButton);
        document.body.appendChild(postContainer);
    });
    function savePost(house, content, imageSrc) {
        if (!content.trim() && !imageSrc) {
            alert('Post content or image cannot be empty!');
            return;
        }
        let postsByHouse = JSON.parse(localStorage.getItem('postsByHouse')) || {};
        if (!postsByHouse[house]) {
            postsByHouse[house] = [];
        }
        postsByHouse[house].push({ content: content.trim(), image: imageSrc, timestamp: new Date().toISOString() });
        localStorage.setItem('postsByHouse', JSON.stringify(postsByHouse));
    }
    function displayPosts(house) {
        const postsContainer = document.getElementById('postsContainer');
        postsContainer.innerHTML = '';
        let postsByHouse = JSON.parse(localStorage.getItem('postsByHouse')) || {};
        let posts = postsByHouse[house] || [];
        posts.forEach(post => {
            const postDiv = document.createElement('div');
            postDiv.classList.add('post-container');
            postDiv.innerHTML = `<p>${new Date(post.timestamp).toLocaleString()}: ${post.content}</p>`;
            if (post.image) {
                const img = document.createElement('img');
                img.src = post.image;
                img.classList.add('image-preview');
                postDiv.appendChild(img);
            }
            postsContainer.appendChild(postDiv);
        });
    }
    document.addEventListener('DOMContentLoaded', () => {
    const selectedHouse = localStorage.getItem('selectedHouse');
    if (selectedHouse) {
        renderHousePage(selectedHouse);
        displayPosts(selectedHouse);
    } else {
        renderDefaultPage(); // Or redirect to a selection page if no house is selected
    }
});

// Select the button and posts container
const clearPostsButton = document.getElementById('clearPostsButton');
const postsContainer = document.getElementById('postsContainer');

// Function to clear all posts
clearPostsButton.addEventListener('click', function() {
    // Clear the content inside the posts container
    postsContainer.innerHTML = '';

    // Clear the posts from localStorage
    const savedHouse = localStorage.getItem('selectedHouse');
    if (savedHouse) {
        let postsByHouse = JSON.parse(localStorage.getItem('postsByHouse')) || {};
        postsByHouse[savedHouse] = []; // Set the posts array for the current house to an empty array
        localStorage.setItem('postsByHouse', JSON.stringify(postsByHouse));
    }
});


</script>
