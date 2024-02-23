---
permalink: animations/spin
layout: page
title: spin
---

<div class="spin-once" id="example">
    spin
</div>

<div style="display:flex; gap:5px;">
    <input type="checkbox" id="infinite">
    infinite
</div>

<style>
    /* spin.css */
    @keyframes spin {
        from {
            transform: rotate(0deg);
        }

        to {
            transform: rotate(360deg);
        }
    }

    .spin {
        animation: spin 2s linear infinite;
    }
    /* spin-once.css */
    .spin-once {
        animation: spin 2s linear;
    } 
    /* example */
    #example {
        display: flex;
        align-items: center;
        place-content: center;
        background-color: red;
        color: white;
        width: 40vw;
        max-width: 400px;
        height: 40vw;
        max-height: 400px;
    }
</style>

<script>
    infinite = document.getElementById("infinite")
    example = document.getElementById("example")
    infinite.addEventListener('change', ()=>{
        example.classList.toggle("spin")
        example.classList.toggle("spin-once")
    })
</script>