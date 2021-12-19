# Koma CryptoCurrency
## Made with Firebase-Firestore and MUI

### Demo - https://koma-crypto.netlify.app/

<ul>Dependencies 
<li>material-ui</li>
<li>material-ui/lab</li>
<li>axios</li>
<li>chart.js</li>
<li>firebase</li>
<li>react-alice-carousel</li>
<li>react-chartjs-2</li>
<li>react-google-button</li>
<li>react-html-parser</li>
</ul>

Security rules for Firestore:
<hr>
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
  
    match /watchlist/{userId}{
      allow read:if isLoggedIn(userId)
      allow write:if request.auth.uid == userId
    }
  }
  function isLoggedIn(userId) {
  	return request.auth.uid == usedId
  }
}

<img src='1.png'/>
<img src='2.png'/>