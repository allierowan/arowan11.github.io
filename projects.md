---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
<h3 class="projects"> Projects </h3>
<h4 class="project-header">
  <a href="#" onclick="toggle_visibility('ydr-descr');">The Yellow Dirt Road</a>
  <small><a href="https://github.com/tiy-trailblazers/trailblazers">Github</a></small>
</h4>

<div id="ydr-descr">
  <p>
    For my final project for the Iron Yard, I paired up with a front-end student to build <a href="https://yellow-dirt-road.herokuapp.com/#/">The Yellow Dirt Road</a>. The Yellow Dirt Road is a hiking and camping trip planner that provides users with an interactive map of trails and campgrounds that they can search in a variety of ways, including by name, location, and length. Users can create a new trip to save in their profiles by adding trails and campgrounds to a prospective trip.
  </p>

  <a href="https://postimg.org/image/tccbrv293/">
    <img src="https://s23.postimg.org/tp3py1kiz/TYDR.gif" alt="TYDR.gif">
  </a>

  <p>
    The back end of the Yellow Dirt Road was built in Ruby on Rails, and communicates to the front end through endpoints that consume and return JSON. The data is stored in a PostGIS database which allowed me to work with spacial objects such as trail paths and park boundaries. The activerecord-postgis-adaptor gem provides ActiveRecord with access to the features of the PostGIS geospatial database. It extends the standard Postgres adaptor to handle the geospatial features.
  </p>
  <p>
    The data that I got from the Open Street Maps Overpass API was often disjoint - one trail would be sent back in multiple different line-strings with no indication that those segments were a part of the same trail. I developed a method that grouped trails together if they were a part of the same path and had the same name, and then stitched the line-strings together in the correct order.
  </p>
</div>

<h4 class="project-header">
  <a href="#" onclick="toggle_visibility('cake-descr');">Cakewalkers</a>
  <small><a href="https://github.com/tiy-dc-ror-2016-oct/cakewalkers">Github</a></small>
</h4>

<div id="cake-descr">
  <p>
    During "Agency Week" at the Iron Yard, our class pretended to be a dev shop and worked with a "client" to create an app for their bakery. We worked together as a team using Github branching and pull requests for version control. We kept in sync with daily stand ups and 2-day sprints. The project lasted one week.
  </p>
  <p>
    The application was built in Ruby on Rails. There are three types of users: admins, cakewalkers, and clients. We made use of the Cancancan gem to limit their different abilities. Clients can create logins, place orders for baked goods, and see the status of their orders. Cakewalkers can claim orders from a list of active, unclaimed orders, mark them out for delivery, and mark them as delivered. Admins can see all past orders, see the cakewalker's queue, and manage the products that are for sale. We used the Stripe gem in test mode to mimic the credit card payment process.
  </p>
  <p>
    When the order has been placed, the app sends a POST request to an API that our instructor built that fakes the responses of an automated baking "robot." It also responds to GET requests for status updates and manages the queue of outstanding orders. We used the estimated time to completion that we received from the robot to pass an estimated delivery time along to the client. You can find the live site on <a href = "https://cakewalkers.herokuapp.com/">Heroku</a>.
  </p>
</div>
<h4 class="project-header">
  <a href="#" onclick="toggle_visibility('forgeddit-descr');">Forgeddit</a>
  <small><a href="https://github.com/arowan11/forgeddit-hw">Github</a></small>
</h4>
<div id="forgeddit-descr">
  <p>
    Forgeddit was an Iron Yard assignment in which we were tasked with creating a Reddit-style rails app. Users can post "shares" to the stream, comment on them, and up and down vote them. They can edit and delete their own comments and shares, and edit their own profile. The title of the post links to the webpage that is being shared. The title of a share may be no longer than 200 characters and the link must be a valid web link.
    <br>
    <br>
    The site was published live to <a href="https://secure-bastion-40242.herokuapp.com/">Heroku</a>.
  </p>
</div>
<p class='footer'>
  You can find more of my work on <a href= "https://github.com/arowan11/">github</a>.
</p>
