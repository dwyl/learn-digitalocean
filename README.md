![Digital Ocean Logo](http://i.imgur.com/VbLgu2p.jpg)


A quick guide to getting a DigitalOcean account and launching your first Droplet (VM) with a simple Node.js APP.

## Why?

Because AWS is so last week.

(No, seriously, have you ever tried asking AWS support a question?
  Unless you are paying them tens of thousands of dollars a month
  and have a "support agreement" your questions just go into
  their ticket system to be forgotten... DigitalOcean not only
  have a great platform, they have a great set of resources and
  a team of people on Twitter ready to answer any question.)

#### Real Reasons:

- A **simpler** way to deploy your apps/websites.
- **Great performance**
- ***Cheaper*** than AWS, Rackspace, etc. ([*transparent pricing*](https://www.digitalocean.com/pricing/))
- Great dashboard for visualising resource usage (RAM/Disk/Network)
- Simple [**API**](https://developers.digitalocean.com/) can be used to
monitor your VMs and scale when required.

## What?

DigitalOcean is a virtual private server provider with a difference:
they have *dramatically* simplified the process.

#### Read More

- http://en.wikipedia.org/wiki/DigitalOcean
- https://www.digitalocean.com/features/technology


## How ?

### Create Account

> Visit: https://www.digitalocean.com and **Create Account**


Enter your billing info (credit card):

![digital ocean billing](http://i.imgur.com/VJGrSUA.png)

### Add your SSH Key

If you want to access your VM without having to remember
(or copy-paste) a password, you will need to follow the
instructions to add your SSH keys *before* creating your
"Droplet" (VM).

![DigitalOcean Add SSH Keys](http://i.imgur.com/5HNevKr.png)


### Create your First "Droplet" (Virtual Machine)

Pick the cheapest VM and which ever region is closest to you.
(to reduce code/file upload time and web latency)

![Create Droplet part 1](http://i.imgur.com/O2MiBam.png)

Next, select your desired Operating System.
(For simplicity we are choosing Ubuntu this time)

![Create Droplet part 2](http://i.imgur.com/lXHc9va.png)

Finally, add your SSH key to the droplet and Click:
**Create Droplet!**

Watch as DigitalOcean starts up your VM:

![Digital Ocean booting](http://i.imgur.com/vC9EJdU.png)


Once this is started you should now see an *overview* of your VM:

![Digital Ocean overview](http://i.imgur.com/lAqDb9A.png)

Locate the IP Address of your VM and copy it into your clip-board

Open your terminal application and login via SSH:

![Digital Ocean Login SSH](http://i.imgur.com/u02XRfV.png)

Now (while logged into the VM via SSH)
run the following commands (in order) in your terminal:
```sh
apt-get update
apt-get install -y git nodejs node npm
npm install n -g
n stable
git clone https://github.com/nelsonic/ac.git
cd ac
npm install
nodejs example/server.js
```

Now visit: IP-Address-of-Your-VM:Port-number
e.g: http://178.62.49.216:3000

> Type a word and watch it auto-suggest!

![Autocomplete](http://i.imgur.com/Tf9jiwR.png)
