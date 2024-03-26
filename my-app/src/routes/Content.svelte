<script>
  import Visited from './Visited.svelte';
 
  import { onMount } from 'svelte';
  
    let dropdowns = [
      { heading: 'Special Features', text: `
      <b>Foundation Year :</b><br/>
       500-1000 years old. <br/>
      <b>Sthala Tree</b> <br/>
      <b>Theertham</b><br/>
      Palsunai, Padma theertham, Sengothai Sunai, Kannimar Sunai, Pasumani Sunai<br/>
<b>Ratham</b><br/>
    <b>Architecture</b><br/>
Dravidian Architecture<br/>
<b>Other Speciality</b><br/>
All merciful Lord Ranganatha appears in a standing form facing east pleasing the mind of His devotees.<br/> 
`
 },
      { heading: 'Sthala Puran', text: `
      Maharshi Kalava was in penance for a quite number of years to have the darshan of Lord Narayana.  One Durmadhan, son of a Gandarva Viswasu by name was bathing in the tank with his wives.  Maharshi Vasishta was returning from Mount Kailash after a darshan of Lord Shiva.  Seeing the sage, Durmadha’s wives stopped bathing and came out of the tank in respect to the sage.  But Durmadha continued bathing nude.  Angry Vasishta cursed Dhurmada to be born a demon.  The wives fell at the feet of Sage Vasishta and begged for relief.  Responding to their prayer, sage said that their husband would be back to them in a short time.



 



Durmadha wandering here and there as a demon saw Maharshi Kalava and began to harass him.  Rishi prayed to Lord Narayana for protection.  Lord granted darshan to Rishi and controlled the demon.  With the touch of Lord, Durmadha was relieved of his curse.  It is believed that this event took place here.



 



The other story is that a king Nanda Boopala, ruling this region renounced his kingdom and set out for penance on Lord Narayana.  His son Darma Gupta became the king and was ruling the region righteously.  When he was in the forest for hunting, dusk set in and the king could not find the way to the camp.  He climbed on a tree and began chanting the Gayatri Mantra.  A bear, chased by a lion also came to the tree branch and sat along with the king.



 



The king said to the bear that both would be at a risk if they returned to the ground.  The bear suggested that the king may sleep half the night when it would take care of him and that it would sleep the remaining night protected by the king.  While the king was sleeping the lion under the tree asked the bear to push the king down.  The bear simply said that it could not commit a sin as breach of trust.  When the kin woke up and the bear started sleeping the lion made the suggestion to the king.  Thoughtlessly, the king obliged the lion pushing the bear down.  Shocked by the behaviour of the king, the bear luckily escaping the attack of the lion, cursed the king to become a lunatic.  King Nanda Boopala seeing the condition of son Darma Gupta, took him to Sage Jaimini for the cure.  Sage suggested that he should have a dip in Palamalai Theertha and worship Lord Ranganatha for recovery.  Darma Gupta was thus saved by Palamalai Lord Ranganatha.
      
      
      ` },
      {heading:'Architecture',text:`All merciful Lord Ranganatha appears in a standing form facing east pleasing the mind of His devotees.  Thumbikkai Azhwar and Mother grace the devotees from their respective shrines.  Adequate space is created around the temple to facilitate car festival and movement of devotees during festival times.  Many visit the temple frequently as the environment and the climate are helpful to keep them healthy and free from any disease.  Irulars, a tribal community are living near the temple.  The car of the temple is aesthetically made by skilled craftsmen.



 



The devotee crowd is huge on new moon days and Saturdays.  There are shrines for Lord Vinayaka, Sri Anjaneya and Acharya Sri Ramanuja.`},
      {heading:'Alanakar of Deity',text:``},
      {heading:'Prayers and Benefits',text:`Special Vratas and Prayers
Those facing the impact of some curses pray for relief.



Offerings to Deity
Devotees perform Tirumanjanam to Lord and Mother with sweet pudding-sarkarai pongal nivedhana.

Stotras and Mantras`},
      {heading:'Festivals',text:`Car festival is celebrated in the temple on Chitra Poornima day in April-May.`},
      {heading:`Social Activities`,text:`<ul><li>Annadhan</li>
        <li>Marriage</li>
        <li>Ear Boring</li>
        <li>Head Shave</li>
        <li>Danaas</li>
        <li>Education Facilities</li>
        <li>Social Drives</li>
        <li>Other Activities</li></ul>`},
      {heading:`Arjita Seva`,text:``}];

    
  

  let mapContainer;

  onMount(() => {
    const map = L.map(mapContainer).setView([51.505, -0.09], 13);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map);

    L.marker([51.5, -0.09]).addTo(map)
      .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
      .openPopup();
  });




      

    let openDropdowns = {};
  
    // Function to toggle dropdown visibility
    function toggleDropdown(id) {
      openDropdowns[id] = !openDropdowns[id];
    }
  
    // Initialize dropdown states
    for (let i = 0; i < dropdowns.length; i++) {
      openDropdowns[i] = false;
    }
  </script>
  


  <style>
    .dropdown {
      margin-bottom: 10px;
      
    }
  
    .dropdown-header {
      font-family: Mukta;
      color:#a50740;
      font-size: 24px;
      font-weight:500;
      padding: 10px;
      background-color: transparent;
      border:None;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  
    .dropdown-content {
      font-family: Mukta;
      color:#000000;
      font-size: 18px;
      padding: 10px;
      display: none;
    }
  
    .dropdown-content.open {
      display: block;
    }
  
    .arrow {
      border: solid #a50740;
      border-width: 0 4px 4px 0;
      display: inline-block;
      padding: 3px;
      margin-right: 10px;
    }
  
    .arrow.down {
      transform: rotate(45deg);
    }
  
    .arrow.up {
      transform: rotate(-135deg);
    }

    .side-heading{
        font-family: Mukta;
      color:#a50740;
      font-size: 24px;
      font-weight:500;
        
    }
  

    @media (min-width: 768px) {
      .container {
        display: flex;
        justify-content: space-between;
      }
  
      .section {
        width: 70%;
        margin:10px;
      }
  
      .info {
        width: 30%;
        background-color: #f8f8f8;
        border:solid 1px #f8e8e8e8;
        padding:15px;
        margin:20px;
      }
    }
  
    @media (max-width: 767px) {
      .section, .info {
        width: 100%;
      }
    }
  </style>


  
  
  <div class="container">
    <div class="section">
        {#each dropdowns as dropdown, index (index)}
        <div class="dropdown">
          <button class="dropdown-header" on:click={() => toggleDropdown(index)} aria-expanded={openDropdowns[index]} aria-controls={`content-${index}`}>
            <i class="arrow {openDropdowns[index] ? 'up' : 'down'}"></i>
            <span>{dropdown.heading}</span>
          </button>
          {#if openDropdowns[index]}
            <div class="dropdown-content open" id={`content-${index}`}>
              <p>{@html dropdown.text}</p>
            </div>
          {/if}
        </div>
      {/each}
    </div>
  
    <div class="info">
        <Visited/>
      <div>
        <h2 class="side-heading">Location</h2>
        <p>Unnamed Road, Anbu Nagar, Podanur, Coimbatore, Tamil Nadu 641023</p>
        <!-- OpenStreetMap API here -->
        <div id="map" bind:this={mapContainer} style="height: 180px;"></div>
      </div>
      <div>
        <h2 class="side-heading">Open Timings</h2>
        <p>All days: 07:00 am - 09:00 am</p>
      </div>
      <div>
        <h2 class="side-heading">Pooja Timings</h2>
        <!-- Pooja timings here -->
      </div>
      <div>
        <h2 class="side-heading">Other Deities</h2>
        <!-- Other deities here -->
      </div>
      <div>
        <h2 class="side-heading">Amenities</h2>
        <ul>
          <li>✔️ Drinking Water</li>
          <li>✔️ Pooja Item Shops</li>
          <li>✔️ Restaurants Nearby</li>
          <li>✔️ Restroom</li>
        </ul>
      </div>
      <div>
        <h2 class="side-heading">How to reach?</h2>
        <p>Nearest Bus Station 🚌 Gandhipuram</p>
        <p>Nearest Railway Station 🚄 Coimbatore</p>
        <p>Nearest Airport ✈️ Coimbatore</p>
      </div>
      <div>
        <h2 class="side-heading">Contact Details</h2>
        <p>Name</p>
        <p>Phone: +91-94433 48564</p>
        <p>Name</p>
        <p>Phone: +91-94433 48564</p>
        <p>Website: ...</p>
      </div>
    </div>
  </div>
  
