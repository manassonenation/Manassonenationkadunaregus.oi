frappe.ready(function() {
    // if (!localStorage.getItem('cookieConsent')) {
    //     document.getElementById('cookieConsent').style.display = 'block';
    // }

    const showNotice = () => {
        if (!localStorage.getItem('dontShowNotice')) {
            $('#noticeModal').modal('show');
        }
    };

    $('#dontShowAgain').on('change', function() {
        if ($(this).is(':checked')) {
            localStorage.setItem('dontShowNotice', 'true');
        } else {
            localStorage.removeItem('dontShowNotice');
        }
    });

    // Show modal when page loads
    showNotice();
});

// function acceptCookies() {
//     localStorage.setItem('cookieConsent', 'accepted');
//     document.getElementById('cookieConsent').style.display = 'none';
//     frappe.show_alert({
//         message: 'Cookie preferences saved',
//         indicator: 'green'
//     });

    
// }

// function declineCookies() {
//     localStorage.setItem('cookieConsent', 'declined');
//     document.getElementById('cookieConsent').style.display = 'none';
//     frappe.show_alert({
//         message: 'Cookie preferences saved',
//         indicator: 'orange'
//     });
// }

