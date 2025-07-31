// Select all sections
const sections = document.querySelectorAll('.section');
// const supportButton = document.querySelector('#support-button');

// Define hover animations
sections.forEach(section => {
  section.addEventListener('mouseenter', () => {
    if (section.classList.contains('content-left')) {
      section.style.clipPath = 'polygon(0 10%, 100% 0, 100% 90%, 0 100%)';
      section.style.backgroundColor = '#28a745'; // Green
    } 
    else if (section.classList.contains('content-right')) {
        section.style.clipPath = 'polygon(0 10%, 100% 0, 100% 90%, 0 100%)';
        // section.style.clipPath = 'polygon(0 0, 100% 10%, 100% 100%, 0 90%)';
    //   section.style.clipPath = 'polygon(0 0, 100% 10%, 100% 100%, 0 90%)';
      section.style.backgroundColor = '#000'; // Yellow
    }
  });

  section.addEventListener('mouseleave', () => {
    if (section.classList.contains('content-left')) {
        // section.style.clipPath = 'polygon(0 10%, 100% 0, 100% 90%, 0 100%)';
      section.style.clipPath = 'polygon(0 0, 100% 10%, 100% 100%, 0 90%)';
      section.style.backgroundColor = '#28a745'; // Original red}
    }
    else if (section.classList.contains('content-right')) {
        section.style.clipPath = 'polygon(0 0, 100% 10%, 100% 100%, 0 90%)';
        // section.style.clipPath = 'polygon(0 10%, 100% 0, 100% 90%, 0 100%)';
      section.style.backgroundColor = '#000'; // Original blue
    }
  });
});


window.onload = (event) => {
  if (!localStorage.getItem('cookieConsent')) {
      const cookieElement = document.getElementById('cookieConsent');
      if (cookieElement) {
          cookieElement.style.display = 'block';
      }
  }

  const showNotice = () => {
      if (!localStorage.getItem('dontShowNotice')) {
          const noticeElement = document.getElementById('noticeModal');
          if (noticeElement) {
              noticeElement.style.display = 'block';
          }
      }
  };

  showNotice();
};

function acceptCookies() {
    localStorage.setItem('cookieConsent', 'accepted');
    document.getElementById('cookieConsent').style.display = 'none';
    frappe.show_alert({
        message: 'Cookie preferences saved',
        indicator: 'green'
    });

    
}

function declineCookies() {
    localStorage.setItem('cookieConsent', 'declined');
    document.getElementById('cookieConsent').style.display = 'none';
    frappe.show_alert({
        message: 'Cookie preferences saved',
        indicator: 'orange'
    });
    localStorage.clear();
}

// function handleLogout() {
//   // Use frappe.call to call the logout method and handle the response
//   frappe.call({
//     method: 'logout',
//     callback: function(response) {
//       // Only redirect after the logout is complete
//       window.location.href = '/home';
//     }
//   });
// }

function handleLogout() {
  // Navigate to the logout endpoint
  window.location.href = '/api/method/logout?redirect-to=/home';
}