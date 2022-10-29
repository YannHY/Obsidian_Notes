---
tags: [Tutorial, Parents]
---

[Document complet (Four tutorials for a better use of electronic devices)](https://docs.google.com/document/d/13hareQVIocwF38e_kvmLFhOvapg1y7T4k5ONcyTO9l0/edit#heading=h.c27527z6rnuj)

- [[How to avoid distraction from the iPad during class]]
- [[Family Link]]
- [[How to Reduce Screen fatigue]]

<hr />

Your children have been given a brand new iPad. And while you may be happy that they are provided with an appropriate ICT education, you may have some concerns about what they will be doing with their new device: will your children do their homework? Will they be watching YouTube videos or playing games for long hours?

As a matter of fact, maybe, as a parent, you feel that you are completely blind and unaware of how the iPad is being used by your children. And surely you want to know how you can keep control of that or check from time to time their screen usage!

So I would like to help by providing some advice about how to monitor your child’s iPad. And to do that, you may use Screen Time.

Among other things.

## Screen Time

[Screen Time](https://support.apple.com/en-us/HT208982) is a feature launched in 2018 in iOS 12. It records the amount of time a user spends on apps or websites. Screen Time also provides blocking features to limit the usage of apps or set restrictions.

### 1. Turn on Screen Time directly on a device

There are two ways you can set up Screen Time controls. This is the first one.

On your child’s device, go to `Settings` > `Screen Time` and tap `Turn On Screen Time`.

![](ScreenTime.png)

Tap `Continue`.

![](TurnOn.png)

Select `This is My Child's [device]`.

![](ThisIsMyChild.png)

For now, you can skip the few following steps, but, of course, setting a passcode will avoid the settings to be bypassed.

![](Documentation/Google/Images/Google%20Classroom/Code.png)

### 2. Turn on Screen Time through Family Sharing

But in my opinion, if you already possess your own iPad or iPhone, the best option is to first create an Apple ID for your child. To do that, you need Family Sharing [^1]. This is the second method to set up Screen Time.

![](FamilySharing.png)

On your device, go to `Settings` and tap on your name. Then choose `Family Sharing` and `Add Family Member`. Tap on `Create a Child Account` and follow the instructions.

![](FamilySharing1.png)
![](FamilySharing2.png)
![](FamilySharing3.png)

So your child will have an Apple ID and be a part of the [Family Sharing](https://support.apple.com/en-us/HT201084) but most importantly you will be able to manage your child’s screen usage within Screen Time from your own device.

It means that all controls are located on your device. You can then control apps your children are using. You can access your children's Activity Report to understand where they spend their time and you can set App Limits...

### How to use Screen Time

![](ScreenTimeSettings.png)

In Settings, you can manage:

1. Downtime
2. App Limits
3. Communication Limits
4. Always allowed
5. Content & Privacy Restrictions

#### 1. Downtime

Scheduling downtime means that it’s time to go to bed or do something else away from the screen. During downtime, if your child tries to use the iPad, he or she gets a message informing that it’s scheduled downtime. If your child tries to access their device during downtime, they can request more time from you.

![](Downtime.png)
![](Downtime2.png)

#### 2. App Limits

Set the amount of time per day that you want your child to spend on certain categories of apps (Games, Entertainment, Productivity, Social Networking, etc.).

![](AppLimits1.png)
![](AppLimits2.png)
![](AppLimits3.png)
![](AppLimits4.png)

You may have noticed from the screenshots above that I have only selected one category. As a matter of fact, I suggest you do the same and apply limits category by category. Of course, you can select everything and say that your child won’t use the iPad more than 1 or 2 hours per day or maybe half an hour and no more on the tablet. But if you want to change something, you’ll have to erase all your settings and start over. Or if you want your child to spend only 30 minutes on YouTube but 1 hour on Books, it’s much more convenient to have settings category by category and therefore to add a new limit.

![](AppLimits6.png)

You can apply limits to apps but you can also add limits to websites as well.

![](AppLimits7.png)

#### 3. Communication Limits

You can set communication limits which only apply to Phone, FaceTime, Messages and iCloud contacts. So you can control who your children can communicate with. This can be with everyone or with people in your contacts.

![](CommunicationLimits.png)

As Apple warns, “Communication to known emergency numbers identified by your carrier is always allowed.”

#### 4. Always Allowed

Specific apps, even if it's downtime or if you set the `All Apps & Categories` app limit, are always available. This could be Messages or FaceTime and, of course, Phone so that your child we’ll be able to reach you no matter what.

![](AlwaysAllowed.png)

#### 5. Content & Privacy Restrictions

We use a Mobile Device Management to create and install configuration profiles which means that, thanks to these profiles, some apps are blacklisted, some words or some websites are forbidden.

But you can block inappropriate content as well. You can also prevent your child to purchase or download apps. All you have to do is to toggle on the `Content & Privacy Restrictions` button.

![](Restrictions.png)

You can do a lot of things in that section. We won’t cover everything but you might be interested in knowing that you can create a website whitelist by allowing only specific websites to be seen, for instance.

To do that, go to `Content Restrictions` > `Web Content` > `Allowed Websites Only` > `Add Website`.

![](Restrictions1.png)
![](Restrictions2.png)
![](Restrictions3.png)
![](Restrictions4.png)

## Cut off your Wi-Fi network

There are simple things to do to prevent your children from using their iPad late at night. You can simply ask them to turn off their device at say 9 p.m. Even ask them to put it in a box outside their bedroom for the night.

While this can be a little bit tricky (a child is a hard bargainer when it comes to getting extra time to do whatever he or she needs to do with his or her device), remember your provider (Virgin, BT, EE and so forth) gave you a box you can access to limit the usage of a specific device.

As a matter of fact, you can simply cut off the wifi for your children at a specific hour while you can still have it for your own device.

The way of doing that is not always user-friendly but let me explain how to do it. Unfortunately, I can only get my examples from my own provider which is Virgin Media. However, things shouldn’t be much different from your own box.

![](IP.png)

First of all, open up your favourite browser and type the IP address of your box. This should be something like `192.168.0.1` or maybe `192.168.1.1`.

Then you are asked to provide your credentials login (username and password). Most of the time, they are located right under your box on a sticker.

If you are a customer of Virgin Media go to `Advanced settings` > `Wireless` > `MAC filtering`.

![](MacFiltering.png)

As you probably have guessed, you are going to filter the access of your network by giving the [MAC address](https://en.wikipedia.org/wiki/MAC_address) of the device for which you want to restrict internet access. It’s very simple. Again, let me explain it.

A device has a name (whatever you want) and it has a MAC address which is a sequence of letters and numbers separated by colons. It is a unique identifier assigned by the device manufacturers. There are many ways to find it but you should be able to get it as you may see on the screenshot.

So, to block internet traffic to a specific device, you are simply going to add a filter rule by giving the name of the device and the MAC address of the device. Eventually, you may want to specify when you want this new rule to apply (say from 9 p.m. to 6 a.m.).

![](Filtering.png)
![](Filtering2.png)

## Educate

We saw in the two previous sections of this article that you can prevent your child from doing this or that but, instead of blocking apps or websites, the best option is probably to educate your children and explain what they should and shouldn’t do.

In my opinion, we can’t control everything and I am not sure this is entirely feasible nor desirable. Furthermore, please, keep in mind that setting restrictions can be a problem for your child. Indeed, imagine that you set the amount of time per day that you want your child to spend on YouTube (say half an hour) and a teacher asks students to watch a full documentary during the class. Your child will have no other option to ask for your permission and if he or she can’t contact you, he or she won’t be able to do the work that has been assigned.

Therefore, I do believe we need to put some rules in place but first, we must talk with our children and probably trust them in the first place. To begin with, we may grant them great liberty in the use they make of their iPad, and if and only if they take advantage of this liberty, maybe we should consider setting restrictions.

[^1]: To learn more about Family Sharing, [visit this page](https://www.apple.com/family-sharing/).