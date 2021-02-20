Readings
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

Reading
“The Past, Present, and Future of Local Storage for Web Applications”


From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object.

function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype. 

interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};

STORAGE EVENT OBJECT PROPERTY	TYPE	DESCRIPTION
key	string	the named key that was added, removed, or modified oldValue	any	the previous value (now overwritten), or null if a new item was added
newValue	any	the new value, or null if an item was removed url*	string	the page which called a method that triggered this change
