<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Enhancing HTML5 Content & Mastering Forms</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body { font-family: Arial, sans-serif; margin: 2em; }
    main { max-width: 750px; margin: auto; }
    section { margin-bottom: 2em; }
    table { border-collapse: collapse; width: 100%; margin-top: 1em; }
    th, td { border: 1px solid #ccc; padding: 8px; text-align: left; }
    fieldset { margin-bottom: 1em; padding: 1em; border-radius: 5px; }
    legend { font-weight: bold; }
    label { display: block; margin-bottom: 0.5em; }
    input, select, textarea { width: 100%; padding: 0.5em; margin-bottom: 1em; }
    .media { display: flex; gap: 2em; flex-wrap: wrap; align-items: center; }
    .media > * { flex: 1 1 250px; }
    .required { color: #d00; }
  </style>
</head>
<body>
  <main>
    <header>
      <h1>Enhancing HTML5 Content & Mastering Forms</h1>
      <p>This web page demonstrates advanced HTML5 content elements and a complete HTML5 form with native validation.</p>
    </header>

    <section>
      <h2>Organizing Content with Lists</h2>
      <ul>
        <li>Semantic HTML improves accessibility</li>
        <li>Lists structure information logically</li>
        <li>Tables present data clearly</li>
      </ul>
      <ol>
        <li>Use <code>&lt;ul&gt;</code> for unordered lists</li>
        <li>Use <code>&lt;ol&gt;</code> for ordered lists</li>
        <li>Use <code>&lt;dl&gt;</code> for description lists</li>
      </ol>
      <dl>
        <dt>Accessibility</dt>
        <dd>Ensures content is usable by all users, including those with assistive technologies.</dd>
        <dt>Semantic Tags</dt>
        <dd>Provide meaning and structure to the document.</dd>
      </dl>
    </section>

    <section>
      <h2>Displaying Data in Tables</h2>
      <table>
        <caption>Sample Course Schedule</caption>
        <thead>
          <tr>
            <th>Day</th>
            <th>Topic</th>
            <th>Activity</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Monday</td>
            <td>HTML Semantics</td>
            <td>Lecture</td>
          </tr>
          <tr>
            <td>Tuesday</td>
            <td>Tables & Lists</td>
            <td>Workshop</td>
          </tr>
          <tr>
            <td>Wednesday</td>
            <td>Forms & Validation</td>
            <td>Lab</td>
          </tr>
        </tbody>
      </table>
    </section>

    <section>
      <h2>Embedding Media</h2>
      <div class="media">
        <figure>
          <img src="https://via.placeholder.com/220x140?text=Sample+Image" alt="Sample Placeholder Image" width="220" height="140">
          <figcaption>Example Image</figcaption>
        </figure>
        <figure>
          <audio controls>
            <source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
          </audio>
          <figcaption>Sample Audio</figcaption>
        </figure>
        <figure>
          <video width="220" height="140" controls>
            <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
            Your browser does not support the video tag.
          </video>
          <figcaption>Sample Video</figcaption>
        </figure>
      </div>
    </section>

    <section>
      <h2>Contact & Registration Form</h2>
      <form action="#" method="post" autocomplete="on">
        <fieldset>
          <legend>Personal Information</legend>
          <label for="name">Full Name <span class="required">*</span></label>
          <input type="text" id="name" name="name" required minlength="2" maxlength="40" placeholder="Enter your name" autocomplete="name">
          
          <label for="email">Email Address <span class="required">*</span></label>
          <input type="email" id="email" name="email" required placeholder="e.g. user@example.com" autocomplete="email">
          
          <label for="dob">Date of Birth</label>
          <input type="date" id="dob" name="dob" min="1900-01-01" max="2025-12-31" autocomplete="bday">
        </fieldset>

        <fieldset>
          <legend>Account Details</legend>
          <label for="username">Username <span class="required">*</span></label>
          <input type="text" id="username" name="username" required pattern="^[a-zA-Z0-9_]{4,16}$" minlength="4" maxlength="16" placeholder="4-16 chars, letters/numbers/_" autocomplete="username">
          
          <label for="password">Password <span class="required">*</span></label>
          <input type="password" id="password" name="password" required minlength="8" maxlength="32" placeholder="At least 8 characters" autocomplete="new-password">
          
          <label for="confirm">Confirm Password <span class="required">*</span></label>
          <input type="password" id="confirm" name="confirm" required minlength="8" maxlength="32" placeholder="Repeat password" autocomplete="new-password">
        </fieldset>

        <fieldset>
          <legend>Preferences</legend>
          <label for="fav-lang">Favorite Language</label>
          <select id="fav-lang" name="fav-lang">
            <option value="">Select one</option>
            <option value="html">HTML</option>
            <option value="css">CSS</option>
            <option value="js">JavaScript</option>
          </select>
          
          <label>
            <input type="checkbox" name="subscribe" value="yes" checked readonly>
            Subscribe to updates (mandatory)
          </label>
        </fieldset>

        <fieldset>
          <legend>Feedback</legend>
          <label for="feedback">How did you find this assignment?</label>
          <textarea id="feedback" name="feedback" rows="4" maxlength="250" placeholder="Your feedback is appreciated"></textarea>
        </fieldset>

        <button type="submit">Submit Registration</button>
      </form>
    </section>
  </main>
</body>
</html>