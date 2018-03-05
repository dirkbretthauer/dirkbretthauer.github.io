---
layout: post
title: grep command for Powershell users
github_comments_issueid: "2"
---

As a former unix user, I wanted to have a similar (single) command to search for content in files in my scripting environment, which is the Powershell. The solution is a pretty simple usage of the two cmdlets Get-ChildItem and Select-String:

{% highlight posh %}
function grep([string]$Path, [string]$Pattern, [string]$FilePattern)
{
    Get-ChildItem -Path $Path -Filter $FilePattern -Recurse | Select-String -Pattern $Pattern
}
{% endhighlight %}

Put this function in to your Powershell profile.ps1 and use it like this:

{% highlight posh %}
grep -Path . -FilePattern *.txt -Pattern findme
{% endhighlight %}

In this example the grep command will search all *.txt files in the current directory and all subdirectories, which have 'findme' in their content.

Have fun and happy searching!
