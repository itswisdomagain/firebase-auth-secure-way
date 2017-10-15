Firebase Authentication - The secure way
=================================================================================

**Authentication** is a very important feature of sensitive applications - web, mobile or desktop. Authentication often goes hand in hand with __Authorization__; whereas the former is used to VERIFY THE IDENTITY of a user of a platform, the latter is used to permit or reject ACCESS to resources based on the identity of the entity requesting the resource.

Firebase helps developers to easily and quickly implement authentication features logic in their applications, giving them time and room to focus on other more platform-specific logic. Every productive developer should want to take this approach.

The default approach to using Firebase Authentication though has a security risk which can be mitigated. What is this default implementation approach and what is the risk associated with it? What can be done to mitigate this risk? That's the body of this talk.

## The default approach.
**AUTHENTICATION** is implemented using the client SDKs for Android, iOS or Web client SDKs.
Perform **AUTHORIZATION** on your server using the Firebase Admin SDK for Node.js, Python, Java or GO.

## The security risk
The aim of authentication is to **AFFIRMATIVELY VERIFY THE IDENTITY OF USERS**. This aim can easily be defeated in client applications. Client applications can be easily modified; and when you entrust the entire AUTHENTICATION process to a client application, you expose your authentication logic to the world and it doesn't require a lot of smarts to weaken the authentication layer by modifying the client application. With Firebase, you may not even need to _modify_ the client application; just grab the keys and you're good to go. And your server could be easily fooled into serving requests for and permitting resources to a user that was not properly authorised.

## Mitigating the risk
Move core authentication logic to your server!

## How can this be done?
This is actually an abstract for a talk I intend to give at GDG DevFest 2017 in Aba and Ibadan :smiley: . I'll update this repo with slides, guides and perhaps sample codes subsequently.

## Extras
Learn how to use the core principles highlighted in this talk to extend the power of Firebase Authentication to yet officially un-supported server-side languages like PHP and ASP.

## Why I'm an authority on this topic
I've delved pretty deep into Firebase Authentication
- Contributor to [Firebase Authentication for .NET SDK](https://github.com/step-up-labs/firebase-authentication-dotnet)
- Wrote [Server-side Firebase Authentication for Node.js SDK](https://github.com/ThisIsRudigo/firebaseauth)
- Currently building a Server-side Firebase Authentication for Java SDK with a friend and colleague as part of a project: [Nearbuy](https://admin.nearbuy.ng)