<template>
    <div class="popup">
        <div class="popup-inner">
            <span class="close" @click="$emit('close')">&times;</span>   
        <slot/>
          
        <!-- <button class="popup-close">Close Popup
        </button> -->
        </div>
    </div>
    </template>
    
    
    <script>
    export default{
        name:'PopUpSmall'
    }
    </script>
    
    
    <style >
    .popup {
        position: fixed;
        top: 20px;
        right: 20px;
        background-color: rgba(0, 0, 0, 0.2);
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px;
        z-index: 10000;
        text-align: left;
      }
      
      .popup-inner {
        background-color: #f5f6fa;
        padding: 15px;
        border-radius: 8px;
        width: 300px; /* Adjust width for a smaller popup */
        box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
        position: relative;
      }
      
      .close {
        position: absolute;
        top: 10px;
        right: 10px;
        font-size: 20px;
        cursor: pointer;
        color: black;
      }
      
      .action-buttons {
        display: flex; /* Align buttons side by side */
        gap: 10px; /* Space between buttons */
      }
      
      .action-buttons button {
        padding: 10px;
        border: none;
        border-radius: 4px;
        background-color: #007bff; /* Button background color */
        color: white; /* Button text color */
        cursor: pointer;
        flex: 1; /* Make buttons fill available space evenly */
      }
      
      .action-buttons button:last-child {
        background-color: #dc3545; /* Different color for delete button */
      }
      
    </style>