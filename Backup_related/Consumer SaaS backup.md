## Consumer SaaS Backup - The Backup World's Untamed Swamp Demanding Your Product

I wrote a whole fancy V1 of this document in a Markdown editor that will have to renamed unnamed and which subsequently lost the file. It kind of illustrates the point. Sigh. 

So here's a shorter version:

Consumer backup is terrible. 

Think of all the little bits and pieces of cloud software that we use every day and commit data to, some of which is important:

- To do list managers
- Photo storage buckets
- Google Docs

The problem: 

- A hell of a lot of it is essentially un-backup-able. I mean you can SORT of do it with a lot of scripting and sending in weird GDPR requests but ... eventually you might chart a trajectory like me and just kind of feel permanently low key uncomfortable about the amount of data you're creating in the cloud that you just hope .... doesn't get destroyed.

But isn't the cloud backup? No. The cloud is just somebody else's computer, you fool! (I jest).

Potential vectors to disaster:

- Accidental user deletion (seen it happen, almost watched a startup lose their only copy of a collaborative file system with literally years of work on it)
- User lockout. With 2FA and the occasional bugginess in 2FA this isn't as far fetched as it might seem. Let's be honest. Who actually bothers to download those text backup codes? Just me then. Okay...
- Ransomware propagation from local to cloud. It happens. 
- Sometimes that amazing new SaaS provider you've discovered is some dude in the great beyonds of Northern Denmark running the thing off an Raspberry Pi and hoping nobody notices how sluggish the infra is. Then said server dies. No, Peder wasn't taking user backups. Yes, it said so in the T&Cs. Yes, this is actually kind of standard. Yes, he's awfully sorry about the whole thing. No, you're not getting your wedding photos back from PhotoBomb.

## Your Job 

**Your mission is to make the Zapier of Backup.**

To do this, you're going to have to go out and talk to every major cloud provider and po-dunk tech startup promising great things and storing user data and hope they'll let you integrate with them. 

Then you're going to allow users to bring their own storage. To get the tecchies into this (because who else thinks about this stuff?) B2 and S3 are absolute musts as backup targets. But you should also support rsync or SSH or whatever will make it easy for users to mirror stuff down to their NAS because that's going to be a lot of the user base for this. 

Then you're going to charge them a monthly sub for access. And you're not going to nickle and dime them with stuff like feature-lock and data egress charges because that will p*ss the target audience off very quickly.

You're going to offer world class support. And you're going to try drive home the message that you shouldn't ever have only one source of important data. Your marketing department's challenge is going to be doing this in a way that doesn't make you sound like a tinfoil hat conspiracy theorist. So you're sort of advocating for cloud-everything while also saying "yeah but still be prudent about it." I think the messages can jam together nicely if you think it through. 

You'll capture a small chunk of the SaaS-using population but that's a gigantic market and they're probably going to be a loyal customer base if you can do this right and build something people actually appreciate and value.