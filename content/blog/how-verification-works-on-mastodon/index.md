---
date: 2022-11-10

title: Reflections - first time manager
subtitle: |
  The challenge of shaping a person's future and career without any formal training - a typical scenario.

summary: |
  Managing can be a formidable task - some may find it effortless
  while others may struggle. Nevertheless, I've gleaned valuable insights
  through my experience, and I'd like to share my key learnings below.

description: |
    my journey managing a non-tech graduate in the tech field of data science.

author: Hamzah Javaid

show_post_date: true
show_author_byline: true

format: hugo

draft: false

freeze: auto
tags:
- Manager
- Reflections

---

**Management is so much more than a team hitting their OKRs and achieving a company’s objective**. You have the power to influence a person’s mental wellbeing, their hopes and desires, their confidence and self-development. Management is coaching, training, mentoring and so much more. At least that was my belief going into the role - I took the role of manager extremely seriously. 

>	"people leave managers not companies"

As a budding philosopher, I always start with “why”. Personally, I find I subscribe to a somewhat deterministic view, and so I asked myself the following questions: 

- Why do I want to be a manager?
- Why this person and why me?
- What is expected of me?
- How do I know if I’ve succeeded, whatever ‘success’ is?

The truth is, I never fully answered these questions but asking the why helped me shape and understand the how. As I now reflect on my first stint as Data Science manager, here are 3 key reflections.


## Don't be dogmatic with Plan A

Winston Churchill famously had the quote:

> “Those who plan do better than those who do not plan, even should they rarely stick to their plan”.

Embedded within this quote is the acknowledgement - it's not alweays possible to stick to your plan. As a first-time manager, I set goals, objectives, and targets for my direct report (DR). I naively assumed they would be followed, but I was wrong. My DR was hard-working and intelligent, but sometimes people prefer to do things their own way. Our project changed and time became limited, but I still pushed my DR to meet the objectives. This approach only made things worse.

Lesson Learned: Having a plan is essential for success, but being able to adapt and have a backup plan is equally important. Flexibility and an open-minded approach to change can ensure that even when things don't go according to plan, the ultimate goal can still be achieved.

------------------------------------------------------------------------

{{< figure src="img/fosstodon-verification.png" caption="A verified link will have a green tick next to its label on your profile." alt="A screenshot of a Mastodon profile with two links in the field section. One of them appears with a green mark next to it." >}}

------------------------------------------------------------------------

## How to set up Mastodon crosslink verification?

To set that up, the only thing one has to do to get the green check mark is to
reference a ressource that has a link back to their Mastodon profile. Be
careful, this link MUST have
[a `rel="me"` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/me).
That is, when I wanted to get a green mark next to my website on
[my Mastodon account](https://fosstodon.org/@cedricbatailler), all I had to do
is to write the following:

    <a rel="me" href="https://fosstodon.org/@cedricbatailler">Mastodon</a>

So, if you like lists:
1. On your website, **put a link to your Mastodon profile** (the link must
have a `rel=me` attribute)
2. Go to **your Mastodon profile**, click **Edit profile**, and, in the
**Profile metadata** section, **add a link to the resource where you put a
link to your Mastodon profile**
3. Profit?

## This is not a Twitter certification

Obviously, this procedure is not exactly like the Twitter certification. It is
free, you can do it on your own, and **it is not there for prestige**. It's
there for security reasons.

In a way, it is closer to a public mail verification (with a website instead
of mail) than the blue badge, but it if you believe that a verification
process should be a security feature, it gets the job done. **By taking 5 minutes
to set that up, you seriously limit the risk of impersonation**. This is
especially relevant on a website that allows anyone to open an account with
the same username as yours on any instance. **Do it**.
