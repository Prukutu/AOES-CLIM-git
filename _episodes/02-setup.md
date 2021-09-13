---
title: Setting Up and Using Git and Github
teaching: 5
exercises: 0
questions:
- "How do I get a Github account?"
- "How do I get set up to use Git on the COLA Computers?"
objectives:
- "Configure `git` "
- "Understand the meaning of the `--global` configuration flag."
keypoints:
-   "Use `git config` with the `--global` option to configure a user name and email address"
---

### GitHub Account

__If you have a GitHub account already, make sure you can find it on the web and can login to it.__

Note that as of September 2021, GitHub is upgrading its security requirements. Your old account may require updating to continue to work. Please see: https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/updating-your-github-access-credentials for options.

These include the following choices:
1. <a href="https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account ">Add existing key to ssh-agent</a> and then <a href="https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh">changing https access to ssh</a>.
2. Remaining with https access but <a href="https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token">creating a personal access token (PAT) for https authentication</a>

There are also instructions for <a href="https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-ssh-to-https">switching a repo’s authentication method between https and ssh</a>.

__If you do not have a GitHub account, create one:__

1. Go to https://github.com, choose a username, email address to use, and password to sign up to Github. 
2. Follow the rest of the instrucitons to create your account.
3. Choose the free service - it is more than adequate for what we will do.

See the links above regarding "security options" for those choices - SSH keys work just like you have set up to log into COLA computers. 
PATs work like passwords.


### Git on Unix

Git is a command line version control system that is available by default on most Unix/Linux, Mac computers and can be easily installed for Windows (https://gitforwindows.org/). You can use it on your own computer.  In this class,  we will be using it on the COLA computers where it is already installed.

When we use Git for the first time,
we need to configure a few things. Below are a few examples
of configurations we will set as we get started with Git:

*   our name and email address,
*   and that we want to use these settings globally (i.e. for every project).

On a command line, Git commands are written as `git verb options`,
where `verb` is what we actually want to do and `options` is additional optional information which may be needed for the `verb`.

First, we can check to see how these options are set by default on the COLA Computers:
~~~
$ git config --list
~~~
{: .language-bash}


Here is how Dracula sets up his new laptop:
~~~
$ git config --global user.name "Vlad Dracula"
$ git config --global user.email "vlad@tran.sylvan.ia"
~~~
{: .language-bash}

Please use your own name and email address instead of Dracula's. This user name and email will be associated with your subsequent Git activity,
which means that any changes pushed to
[GitHub](https://github.com/) will include this information.

For these lessons, we will be interacting with [GitHub](https://github.com/) and so the email address used should be the same as the one used when setting up your GitHub account. If you are concerned about privacy, please review [GitHub's instructions for keeping your email address private][git-privacy]. 

>## Keeping your email private
>
>If you elect to use a private email address with GitHub, then use that same email address for the `user.email` value, e.g. `username@users.noreply.github.com` replacing `username` with your GitHub one.
{: .callout}


These commands we just ran above only need to be run once: the flag `--global` tells Git
to use the settings for every project, in your user account, on this computer.

You can check your settings at any time:

~~~
$ git config --list
~~~
{: .language-bash}

You can change your configuration anytime you want using the same commands.

> ## Git Help and Manual
>
> Always remember that if you forget a `git` command, you can access the list of commands by using `-h` and access the Git manual by using `--help` :
>
> ~~~
> $ git config -h
> $ git config --help
> ~~~
> {: .language-bash}
>
> While viewing the manual, remember the `:` is a prompt waiting for commands and you can press <kbd>Q</kbd> to exit the manual.
>
{: .callout}

[git-privacy]: https://help.github.com/articles/keeping-your-email-address-private/
