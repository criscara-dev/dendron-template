---
id: e869bed8-e44f-44fd-8698-7ac005211ca5
title: '2020-10-18'
desc: ''
updated: 1603018358223
created: 1603018358223
stub: false
---

More I read about Dendron and Hierarchies more I think this is the way the brain is working.
I used to use PARA for less than a year now but it doesn't make sense anymore.
How can they be compatible? (Hiearchies and PARA)
The brain doesn't have 4 folders...not sure either about hierarchies.
If fact what is really an Archive? I have staff in my Archive but who knows if tonight I need something from there... and maybe tomorrow as well.
So, it's a Resource then? Not in Archive as I though.
Wait a minute, before put that stuff into Archive, it used to be a Project, and as I said, I need again soon (even if I didn't need it for a week or a month).

At this point instead of go back and forth from 4 folders maybe make more sense to use Hierarchies and lookups.

My brain in fact works for Area first ( -> first level Parent in my Hierarchy system), moving toward more detailed area.
Even a project is part of an area (in Kevin blog they'd be called 'group related chunks').
Ref: It’s Not You - It’s Your Knowledge Base, Chunking.

ex. kind of a schema here:
my personal view:

Vault  {
.root as ARCHIVE {
    (AREAS)
    .finance {
        .salary {},
        .tax {},
        .savings {};
        general expenses {}
        }
    .health {
        .movement {},
        .nutrition {
            .foods,
            .no-allowed-foods {
                *sugar, *honey (backlink to *high-glycemic-index)
            };
            .supplements,
        },
        .hospitalizations {},
        .blood tests {
            *high-glycemic-index (backlink to *sugar)
        },
        .other exams {}
        }
    .work {
        pro1 {},
        issues with colleagues,
    }
    .social {
        .family {},
        .friends {},
        .colleague {},
        .enemies {}
    }
    .learning {
        .math,
        .programming {
            .lang {
                .js {
                    .api {}
                    .node {}
                },
            .apex {},
            }
            .salesforce {},
        },
    }
    }
 }

The idea here is that Hierarchies for me works better and I think it better integrate with the [Zettelkasten](https://zettelkasten.de/) method.


- Late day thought after online listening and reading about science stuff, #Sabine-Hossenfelder on #Bhomian-Mechanics and https://www.Brilliant.org tasks...
> hidden variables + what I know -> solution
Hidden variables sometimes can be changed with 'intuition' educated guess
Hidden variables can be because I don't know have the tools to answer.
