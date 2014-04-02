---
layout: post
title: Before Genesis
description: "Inserting a post chronologically before the First Post. Video on Meteor.js"
modified: 2014-04-02 13:28:12 -0400
tags: [meteor.js]
image:
  feature: texture-feature-05.jpg
  credit: Texture Lovers
  creditlink: http://texturelovers.com
comments: true
share: true
---

<iframe width="560" height="315" src="//www.youtube.com/embed/lSAKFkxq4jA" frameborder="0"> </iframe>
<br />
Hello there! What's that? A responsive video? :o

<br />

{% highlight js %}
Pomegranates = new Meteor.Collection("Pomegranates", {}); //global variable

if (Meteor.isClient) {
  Accounts.ui.config({
   passwordSignupFields: 'USERNAME_AND_EMAIL'
  });

  Meteor.subscribe('pomegranates'); //matches what's in publish in isServer. define what gets synced to browser.

  Template.hello.greeting = function () {
    return "Welcome to Pomegranate.";
  };

  Template.hello.events({
    'click input': function () {
      // template data, if any, is available in 'this'
      if (typeof console !== 'undefined')
        console.log("You pressed the button");
    }
  });


Template.pomegranatesList.helpers({
    allPomegranates: function () {
       return Pomegranates.find({}, {sort: {startDate: -1}});
     }
   });
 
   Template.pomegranatesList.events({
     'submit #new-pomegranate' : function (e) {
       e.preventDefault(); // don't reload the page like you would by default
                            // instead do some interesting stuff: 
       var pomegranate = {
         userId: Meteor.user()._id, // user id added to document
         startDate: new Date(),
         goal: $(e.target).find('[name=goal]').val(),
       };
       
       Pomegranates.insert(pomegranate);
     },

     'click .delete' : function (e) { //event name is click; selector is anything with delete
      Pomegranates.remove(this._id);
     }
   });
 }

if (Meteor.isServer) {
  // necessary because autopublish was removed
 Meteor.publish("pomegranates", function (){
  return Pomegranates.find({}, {sort: {startDate: -1}}); //return result of this query. define what gets synced to browser.
 });
  // check to see if the appropriate user is signed in to the document
  Meteor.startup(function () {
    var ownsDocument = function(userId, doc) {
  return doc && doc.userId === userId;
 }
 // if current user matches the document, you are allowed to do these things
 Pomegranates.allow({
   insert: ownsDocument,
   update: ownsDocument,
   remove: ownsDocument,
 });
    // code to run on server at startup
  });
}
{% endhighlight %}

<br />
<a href="http://it-ebooks.info/go.php?id=1354-1396471669-dd28748c22b86ed5f0217f88365ad35b" class="btn btn-success">Download a free, unrelated book!</a>

