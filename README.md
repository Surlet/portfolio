<h1>Bed & breakfast booking pattern analysis</h1>

<h2>Overview</h2>

<p>The object of this analysis is the booking data from a bed & breakfast located in Hesbaye region in Belgium. The data comes from the Lighthouse booking software and spans from the opening of the bed & breakfast in 2012 until August 2025. The Hesbaye region is known for its fruit orchards, bucolic landscapes and cycling itineraries. It has become a popular weekend destination for local tourists, mostly coming from other parts of Flanders.</p>
<p>The goal of this analysis is twofold:</p>
<ol type="a">
  <li>Identify key booking patterns</li>
  <li>Determine growth opportunities</li>
</ol>
<p>To achieve this goal, it will be interesting to examine the following metrics:</p>
<ul>
  <li>Cancellation rate</li>
  <li>Booking channels</li>
  <li>Origin of hosts</li>
  <li>Examining booking patterns on weekdays and on weekends</li>
  <li>Examining booking patterns in season and off season</li>
  <li>Understand when guests are reservation: what day, what month, how long in advance</li>
</ul>

<h2>Data cleaning</h2>
<h3>Verifying unique values</h3>

<p>While verifying email-adresses, it became clear that a significant amount of reservations had been made with the email-address of the B&B managers. After questioning them, it appears some of these bookings were made because the customer's email-address was unknown, but on other occasions, these bookings were incorrect and subsequently cancelled. Those incorrect bookings are removed from the data. The same was done with rooms booked on the name of the B&B managers.</p>
<p>The criteria used to delete a record was that:</p>
<ul>
  <li>The reservation was made on the name or email of the B&B managers</li>
  <li>The reservation was cancelled or the price was null</li>
</ul>

<p>The next step is to verify the country of the customer. When scanning for the unique values, it appeared there were different values for the same country. Most of the time, the two-letter ISO code was used, but on certain records, the country name was written in full. I corrected those values in order to have conform data. Additionnally, on two occasions, a city name was filled in instead of the country. This was also corrected.</p>
<img width="88" height="285" alt="image" src="https://github.com/user-attachments/assets/2c4cb639-1735-41f7-9195-69b4eb4118e0" />

<p>The column "Postcode" (Postal Code) is also checked and corrected where needed</p>

<h3>Checking null values</h3>

<p>The record with a null price were removed from the dataset.</p>

<h3>Checking double values</h3>

There are no double ID values or double reservations numbers

<h3>Standardising data types</h3>

The data types of the date and price columns were checked, they were all correct.



