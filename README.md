import os

NAV = [
    ("index.html", "Home"),
    ("about.html", "About"),
    ("services.html", "Programs"),
    ("membership.html", "Membership"),
    ("trainers.html", "Trainers"),
    ("gallery.html", "Gallery"),
    ("testimonials.html", "Testimonials"),
    ("blog.html", "Blog"),
    ("seo.html", "SEO"),
    ("sem.html", "SEM"),
    ("smm.html", "Social Media"),
    ("email-marketing.html", "Email Mktg"),
    ("content-marketing.html", "Content Mktg"),
    ("affiliate-marketing.html", "Affiliate"),
    ("analytics.html", "Analytics"),
    ("digital-strategy.html", "DM Strategy"),
    ("faq.html", "FAQ"),
    ("contact.html", "Contact"),
]

def render_nav(active):
    links = []
    for fname, label in NAV:
        cls = ' class="active"' if fname == active else ''
        links.append(f'<a href="{fname}"{cls}>{label}</a>')
    return "\n      ".join(links)

def page(fname, title, eyebrow, heading, lead, body):
    nav_html = render_nav(fname)
    html = f"""<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>{title} · FlexFit Gym</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<nav class="navbar">
  <div class="nav-inner">
    <a href="index.html" class="logo">FLEX<span>FIT</span></a>
    <div class="navlinks">
      {nav_html}
    </div>
  </div>
</nav>

<header class="page-hero">
  <div class="wrap">
    <div class="eyebrow">{eyebrow}</div>
    <h1>{heading}</h1>
    <p class="lead">{lead}</p>
  </div>
</header>

{body}

<footer>
  <div class="wrap">
    <div class="foot-grid">
      <div>
        <h4>FlexFit Gym</h4>
        <a href="about.html">About Us</a>
        <a href="trainers.html">Our Trainers</a>
        <a href="membership.html">Membership Plans</a>
      </div>
      <div>
        <h4>Digital Marketing Project</h4>
        <a href="seo.html">SEO Strategy</a>
        <a href="sem.html">SEM Strategy</a>
        <a href="smm.html">Social Media Marketing</a>
        <a href="email-marketing.html">Email Marketing</a>
        <a href="content-marketing.html">Content Marketing</a>
        <a href="affiliate-marketing.html">Affiliate Marketing</a>
      </div>
      <div>
        <h4>Insights</h4>
        <a href="analytics.html">Web Analytics</a>
        <a href="digital-strategy.html">Full DM Strategy</a>
        <a href="blog.html">Blog</a>
      </div>
      <div>
        <h4>Support</h4>
        <a href="faq.html">FAQ</a>
        <a href="contact.html">Contact</a>
        <a href="testimonials.html">Testimonials</a>
      </div>
    </div>
    <div class="foot-bottom">Class XII Digital Marketing Practical Project · FlexFit Gym is a fictional brand created for academic purposes</div>
  </div>
</footer>

</body>
</html>
"""
    with open(fname, "w") as f:
        f.write(html)

# ---------------------------------------------------------------
# 1. HOME
# ---------------------------------------------------------------
page(
    "index.html", "Home", "Class XII Digital Marketing Project",
    'TRAIN HARD. <span class="accent">MARKET SMART.</span>',
    "FlexFit Gym is a fictional fitness brand built to demonstrate a complete digital marketing strategy — from the business website itself to SEO, social media, email campaigns, and analytics.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">01</div><h3>Real Business Website</h3><p>A working multi-page gym website covering services, trainers, membership, and community.</p></div>
      <div class="card"><div class="badge orange">02</div><h3>Full DM Toolkit</h3><p>Dedicated pages demonstrating SEO, SEM, Social Media, Email, Content, and Affiliate Marketing strategies.</p></div>
      <div class="card"><div class="badge pink">03</div><h3>Data-Backed Plan</h3><p>An analytics dashboard and a combined digital marketing strategy tying every channel together.</p></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Why FlexFit?</h2>
    <p class="section-sub">A gym built around community, progress tracking, and no-judgment training — the same values carried through every marketing channel.</p>
    <div class="grid cols-4">
      <div class="mock-img mock-1">Strength Zone</div>
      <div class="mock-img mock-2">Cardio Deck</div>
      <div class="mock-img mock-1">Group Classes</div>
      <div class="mock-img mock-2">Recovery Lounge</div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <h2 class="section-title">Explore the Project</h2>
    <p class="section-sub">Jump straight to any part of the digital marketing plan.</p>
    <div class="grid cols-4">
      <a class="card" href="seo.html"><h3>SEO</h3><p>Keyword strategy & on-page optimization</p></a>
      <a class="card" href="smm.html"><h3>Social Media</h3><p>Instagram & YouTube campaign plan</p></a>
      <a class="card" href="email-marketing.html"><h3>Email Marketing</h3><p>Newsletter & retention funnel</p></a>
      <a class="card" href="analytics.html"><h3>Analytics</h3><p>KPIs & performance tracking</p></a>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 2. ABOUT
# ---------------------------------------------------------------
page(
    "about.html", "About Us", "Our Story",
    'ABOUT <span class="accent">FLEXFIT</span>',
    "Founded on the idea that fitness should be accessible, energetic, and community-driven — not intimidating.",
    """
<section>
  <div class="wrap grid cols-2" style="align-items:center;">
    <div>
      <h2 class="section-title">Built By Trainers, For Everyone</h2>
      <p style="color:var(--muted);">FlexFit Gym opened with one goal: make world-class training accessible to beginners and athletes alike. Our certified trainers, functional training zones, and recovery-first philosophy have made us a fitness destination for our city.</p>
      <p style="color:var(--muted);">This site doubles as a Class XII Digital Marketing practical project, showcasing how a local business like FlexFit would plan and execute a real digital marketing strategy.</p>
    </div>
    <div class="mock-img mock-1" style="aspect-ratio:1/1;">Gym Floor Photo</div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Our Mission & Values</h2>
    <div class="grid cols-3">
      <div class="card"><h3>Community First</h3><p>Group classes and events that build accountability, not just muscle.</p></div>
      <div class="card"><h3>Progress Over Perfection</h3><p>Personalized plans that track real, sustainable improvement.</p></div>
      <div class="card"><h3>Science-Backed Training</h3><p>Certified trainers using proven methods, not fitness fads.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 3. SERVICES
# ---------------------------------------------------------------
page(
    "services.html", "Programs", "What We Offer",
    'TRAINING <span class="accent">PROGRAMS</span>',
    "From strength training to recovery therapy — every program is designed around measurable results.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">Strength</div><h3>Strength & Conditioning</h3><p>Free weights, machines, and powerlifting platforms for every level.</p></div>
      <div class="card"><div class="badge orange">Cardio</div><h3>Cardio & HIIT</h3><p>High-intensity interval classes and a full cardio deck.</p></div>
      <div class="card"><div class="badge pink">Group</div><h3>Group Classes</h3><p>Zumba, spin, and functional bootcamps every day of the week.</p></div>
      <div class="card"><div class="badge blue">Personal</div><h3>1-on-1 Personal Training</h3><p>Custom plans with a dedicated certified coach.</p></div>
      <div class="card"><div class="badge lime">Recovery</div><h3>Recovery Lounge</h3><p>Sauna, stretch zone, and physiotherapy consultations.</p></div>
      <div class="card"><div class="badge orange">Nutrition</div><h3>Nutrition Coaching</h3><p>Diet plans built around your training goals.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 4. MEMBERSHIP
# ---------------------------------------------------------------
page(
    "membership.html", "Membership", "Plans & Pricing",
    'CHOOSE YOUR <span class="accent">PLAN</span>',
    "Flexible memberships designed for every stage of your fitness journey.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">Basic</div><h3>₹1,499 / month</h3><p>Full gym floor access, locker facility, and 2 group classes a week.</p></div>
      <div class="card" style="border-color:var(--lime);"><div class="badge orange">Most Popular</div><h3>₹2,499 / month</h3><p>Everything in Basic plus unlimited group classes and 1 nutrition session.</p></div>
      <div class="card"><div class="badge pink">Elite</div><h3>₹4,999 / month</h3><p>All access plus 4 personal training sessions and recovery lounge.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 5. TRAINERS
# ---------------------------------------------------------------
page(
    "trainers.html", "Trainers", "Meet The Team",
    'CERTIFIED <span class="accent">TRAINERS</span>',
    "Every FlexFit coach is certified, experienced, and genuinely invested in your progress.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-4">
      <div class="card"><div class="mock-img mock-1" style="margin-bottom:14px;">Photo</div><h3>Arjun Mehta</h3><p>Strength & Conditioning Coach</p></div>
      <div class="card"><div class="mock-img mock-2" style="margin-bottom:14px;">Photo</div><h3>Sana Kapoor</h3><p>HIIT & Group Class Lead</p></div>
      <div class="card"><div class="mock-img mock-1" style="margin-bottom:14px;">Photo</div><h3>Rohan Verma</h3><p>Personal Training Head</p></div>
      <div class="card"><div class="mock-img mock-2" style="margin-bottom:14px;">Photo</div><h3>Divya Nair</h3><p>Nutrition & Wellness Coach</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 6. GALLERY
# ---------------------------------------------------------------
page(
    "gallery.html", "Gallery", "Inside FlexFit",
    'THE <span class="accent">GALLERY</span>',
    "A look at our facility, classes, and community events.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-4">
      <div class="mock-img mock-1">Weight Room</div>
      <div class="mock-img mock-2">Cardio Deck</div>
      <div class="mock-img mock-1">Group Class</div>
      <div class="mock-img mock-2">Recovery Lounge</div>
      <div class="mock-img mock-1">Locker Rooms</div>
      <div class="mock-img mock-2">Reception</div>
      <div class="mock-img mock-1">Outdoor Yard</div>
      <div class="mock-img mock-2">Community Event</div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 7. TESTIMONIALS
# ---------------------------------------------------------------
page(
    "testimonials.html", "Testimonials", "Member Stories",
    'REAL <span class="accent">RESULTS</span>',
    "Hear from the FlexFit community.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><p style="color:var(--text);">"Lost 12kg in 6 months with the personal training plan. The coaches actually track your progress."</p><h3 style="margin-top:16px;">— Kabir S.</h3></div>
      <div class="card"><p style="color:var(--text);">"The group classes keep me consistent. Best energy of any gym I've trained at."</p><h3 style="margin-top:16px;">— Meera J.</h3></div>
      <div class="card"><p style="color:var(--text);">"Recovery lounge is a game changer after leg day. Highly recommend the Elite plan."</p><h3 style="margin-top:16px;">— Aditya R.</h3></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 8. BLOG
# ---------------------------------------------------------------
page(
    "blog.html", "Blog", "Content Hub",
    'FITNESS <span class="accent">BLOG</span>',
    "Articles published as part of our content marketing strategy — driving organic traffic and building authority.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">Nutrition</div><h3>5 High-Protein Meals Under 15 Minutes</h3><p>Quick recipes to hit your macros without spending hours cooking.</p></div>
      <div class="card"><div class="badge orange">Training</div><h3>Beginner's Guide to Progressive Overload</h3><p>The one principle every strength program should be built on.</p></div>
      <div class="card"><div class="badge pink">Recovery</div><h3>Why Sleep Matters More Than Your Workout</h3><p>The science of recovery and why rest days aren't optional.</p></div>
      <div class="card"><div class="badge blue">Motivation</div><h3>How to Build a Gym Habit That Sticks</h3><p>Habit-stacking techniques from our coaching team.</p></div>
      <div class="card"><div class="badge lime">Cardio</div><h3>HIIT vs Steady-State: What's Better?</h3><p>Breaking down the pros and cons of each training style.</p></div>
      <div class="card"><div class="badge orange">Community</div><h3>Inside Our Monthly Transformation Challenge</h3><p>How members are hitting their goals together.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 9. SEO
# ---------------------------------------------------------------
page(
    "seo.html", "SEO Strategy", "Search Engine Optimization",
    'SEO <span class="accent">STRATEGY</span>',
    "How FlexFit ranks on Google for local, high-intent fitness searches.",
    """
<section>
  <div class="wrap">
    <h2 class="section-title">Target Keyword Research</h2>
    <p class="section-sub">Primary keywords chosen based on local search intent and competition level.</p>
    <table>
      <tr><th>Keyword</th><th>Search Intent</th><th>Monthly Volume (Est.)</th><th>Priority</th></tr>
      <tr><td>gym near me</td><td>Local / Transactional</td><td>High</td><td>Very High</td></tr>
      <tr><td>best gym for beginners</td><td>Informational</td><td>Medium</td><td>High</td></tr>
      <tr><td>personal trainer [city]</td><td>Local / Transactional</td><td>Medium</td><td>High</td></tr>
      <tr><td>gym membership plans</td><td>Commercial</td><td>Medium</td><td>Medium</td></tr>
      <tr><td>HIIT classes near me</td><td>Local / Transactional</td><td>Low-Medium</td><td>Medium</td></tr>
    </table>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">On-Page SEO Checklist</h2>
    <div class="grid cols-2">
      <div class="card"><h3>Title Tags & Meta Descriptions</h3><p>Every page uses a unique, keyword-rich title (e.g. "Membership Plans | FlexFit Gym") and a compelling meta description under 160 characters.</p></div>
      <div class="card"><h3>Header Structure</h3><p>Consistent H1 → H2 → H3 hierarchy across all 18 pages for crawlability.</p></div>
      <div class="card"><h3>Local SEO</h3><p>Google Business Profile optimization, NAP consistency, and local backlinks from city fitness directories.</p></div>
      <div class="card"><h3>Mobile & Speed</h3><p>Fully responsive layout with compressed assets for fast load times — a key Google ranking factor.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 10. SEM
# ---------------------------------------------------------------
page(
    "sem.html", "SEM Strategy", "Search Engine Marketing",
    'SEM <span class="accent">& GOOGLE ADS</span>',
    "Paid search campaigns designed to capture high-intent, ready-to-join leads.",
    """
<section>
  <div class="wrap">
    <h2 class="section-title">Sample Google Ad</h2>
    <div class="mock-post" style="max-width:520px;">
      <div class="platform">Ad · flexfitgym.com</div>
      <h3 style="margin:0 0 6px;">FlexFit Gym — First Week Free</h3>
      <p style="color:var(--muted); margin:0 0 6px;">Certified trainers. Flexible plans. Join the community that keeps you consistent.</p>
      <p style="color:var(--lime); font-size:0.85rem; margin:0;">Sign Up Today →</p>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Campaign Structure</h2>
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">Campaign 1</div><h3>Brand Search</h3><p>Bidding on "FlexFit Gym" and close variants to protect brand traffic.</p></div>
      <div class="card"><div class="badge orange">Campaign 2</div><h3>Local Intent</h3><p>"gym near me", "gym in [city]" — geo-targeted radius of 8km.</p></div>
      <div class="card"><div class="badge pink">Campaign 3</div><h3>Retargeting</h3><p>Display ads for visitors who viewed Membership but didn't sign up.</p></div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <h2 class="section-title">Budget Allocation (Monthly)</h2>
    <table>
      <tr><th>Channel</th><th>Budget</th><th>Goal</th></tr>
      <tr><td>Google Search Ads</td><td>₹15,000</td><td>Lead generation</td></tr>
      <tr><td>Display Retargeting</td><td>₹5,000</td><td>Conversion recovery</td></tr>
      <tr><td>YouTube Pre-roll</td><td>₹5,000</td><td>Brand awareness</td></tr>
    </table>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 11. SMM
# ---------------------------------------------------------------
page(
    "smm.html", "Social Media Marketing", "SMM Strategy",
    'SOCIAL MEDIA <span class="accent">MARKETING</span>',
    "Building community and driving membership through Instagram, YouTube, and Facebook.",
    """
<section>
  <div class="wrap">
    <h2 class="section-title">Sample Instagram Post</h2>
    <div class="mock-post" style="max-width:420px;">
      <div class="platform">Instagram · @flexfitgym</div>
      <div class="mock-img mock-1" style="aspect-ratio:1/1;">Transformation Post</div>
      <p style="margin-top:12px; color:var(--text);">Sarah lost 10kg in 4 months with our Elite plan 💪 Your transformation starts with one workout. #FlexFitResults #GymMotivation</p>
      <div class="stats"><span>❤ 842 likes</span><span>💬 56 comments</span></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Platform Strategy</h2>
    <div class="grid cols-3">
      <div class="card"><div class="badge pink">Instagram</div><h3>Reels & Transformations</h3><p>Daily reels of workouts, form tips, and member transformation stories.</p></div>
      <div class="card"><div class="badge orange">YouTube</div><h3>Full Workout Tutorials</h3><p>Weekly long-form videos on technique, nutrition, and trainer Q&As.</p></div>
      <div class="card"><div class="badge blue">Facebook</div><h3>Community Groups</h3><p>A members-only group for accountability, events, and challenges.</p></div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <h2 class="section-title">Content Calendar (Weekly)</h2>
    <table>
      <tr><th>Day</th><th>Platform</th><th>Content Type</th></tr>
      <tr><td>Monday</td><td>Instagram</td><td>Motivation Reel</td></tr>
      <tr><td>Wednesday</td><td>YouTube</td><td>Workout Tutorial</td></tr>
      <tr><td>Friday</td><td>Instagram</td><td>Member Transformation</td></tr>
      <tr><td>Sunday</td><td>Facebook</td><td>Weekly Recap + Challenge</td></tr>
    </table>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 12. EMAIL MARKETING
# ---------------------------------------------------------------
page(
    "email-marketing.html", "Email Marketing", "Email Campaigns",
    'EMAIL <span class="accent">MARKETING</span>',
    "Nurturing leads and retaining members through targeted email campaigns.",
    """
<section>
  <div class="wrap">
    <h2 class="section-title">Sample Welcome Email</h2>
    <div class="mock-email">
      <div class="email-head">From: FlexFit Gym &lt;hello@flexfitgym.com&gt;<br>Subject: Welcome to the FlexFit Family 💪</div>
      <div class="email-body">
        <h3>Your First Week Starts Now</h3>
        <p>Hey there! We're thrilled to have you join FlexFit. Here's your personalized starter guide, class schedule, and a free nutrition consultation booking link.</p>
        <span class="cta-email">Book My Free Session</span>
      </div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Email Funnel</h2>
    <div class="timeline">
      <div class="step"><h3>Day 0 — Welcome Email</h3><p>Sent immediately after sign-up with onboarding info.</p></div>
      <div class="step"><h3>Day 3 — Class Schedule Reminder</h3><p>Encourages first class booking with a clear call-to-action.</p></div>
      <div class="step"><h3>Day 10 — Progress Check-in</h3><p>Personalized nudge from a trainer to keep engagement high.</p></div>
      <div class="step"><h3>Day 30 — Referral Offer</h3><p>Discount for referring a friend, driving organic growth.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 13. CONTENT MARKETING
# ---------------------------------------------------------------
page(
    "content-marketing.html", "Content Marketing", "Content Strategy",
    'CONTENT <span class="accent">MARKETING</span>',
    "Long-term value content that builds trust and drives organic discovery.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-2">
      <div class="card"><h3>Blog Articles</h3><p>Weekly SEO-optimized articles on training, nutrition, and recovery (see the Blog page) to capture organic search traffic.</p></div>
      <div class="card"><h3>Video Tutorials</h3><p>YouTube workout breakdowns that double as top-of-funnel brand awareness content.</p></div>
      <div class="card"><h3>Free Downloadables</h3><p>A free "4-Week Beginner Plan" PDF offered in exchange for email sign-up.</p></div>
      <div class="card"><h3>User-Generated Content</h3><p>Reposting member transformation stories to build authentic social proof.</p></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Content Pillars</h2>
    <table>
      <tr><th>Pillar</th><th>Goal</th><th>Format</th></tr>
      <tr><td>Education</td><td>Build authority</td><td>Blog, YouTube</td></tr>
      <tr><td>Motivation</td><td>Drive engagement</td><td>Instagram Reels</td></tr>
      <tr><td>Social Proof</td><td>Build trust</td><td>Testimonials, UGC</td></tr>
      <tr><td>Offers</td><td>Drive conversions</td><td>Email, Landing pages</td></tr>
    </table>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 14. AFFILIATE MARKETING
# ---------------------------------------------------------------
page(
    "affiliate-marketing.html", "Affiliate Marketing", "Partnerships",
    'AFFILIATE & <span class="accent">INFLUENCER</span> MARKETING',
    "Extending reach through local fitness influencers and referral partnerships.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-3">
      <div class="card"><div class="badge lime">Micro-Influencers</div><h3>Local Fitness Creators</h3><p>Partnering with 5,000–20,000 follower fitness accounts for authentic reach.</p></div>
      <div class="card"><div class="badge orange">Referral Program</div><h3>Member Referral Codes</h3><p>Existing members get a free month for every friend who joins using their code.</p></div>
      <div class="card"><div class="badge pink">Brand Partnerships</div><h3>Nutrition & Apparel Brands</h3><p>Co-branded giveaways with protein and activewear brands for cross-promotion.</p></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Sample Referral Tracking</h2>
    <table>
      <tr><th>Referrer</th><th>Code</th><th>Signups</th><th>Reward Earned</th></tr>
      <tr><td>Kabir S.</td><td>KABIR10</td><td>4</td><td>1 Free Month</td></tr>
      <tr><td>Meera J.</td><td>MEERA10</td><td>2</td><td>Merch Voucher</td></tr>
    </table>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 15. ANALYTICS
# ---------------------------------------------------------------
page(
    "analytics.html", "Web Analytics", "Performance Tracking",
    'WEB <span class="accent">ANALYTICS</span>',
    "Tracking KPIs across the funnel to measure what's actually working.",
    """
<section>
  <div class="wrap">
    <div class="grid cols-4">
      <div class="stat"><div class="num">12.4K</div><div class="label">Monthly Visitors</div></div>
      <div class="stat"><div class="num">3.8%</div><div class="label">Conversion Rate</div></div>
      <div class="stat"><div class="num">₹210</div><div class="label">Cost Per Lead</div></div>
      <div class="stat"><div class="num">64%</div><div class="label">Member Retention</div></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Traffic Sources</h2>
    <table>
      <tr><th>Source</th><th>% of Traffic</th><th>Avg. Conversion Rate</th></tr>
      <tr><td>Organic Search</td><td>38%</td><td>4.1%</td></tr>
      <tr><td>Instagram</td><td>27%</td><td>3.4%</td></tr>
      <tr><td>Google Ads</td><td>19%</td><td>5.6%</td></tr>
      <tr><td>Direct / Referral</td><td>16%</td><td>6.2%</td></tr>
    </table>
  </div>
</section>

<section>
  <div class="wrap">
    <h2 class="section-title">Tools Used</h2>
    <div class="grid cols-3">
      <div class="card"><h3>Google Analytics 4</h3><p>Tracking user behavior, funnels, and drop-off points.</p></div>
      <div class="card"><h3>Google Search Console</h3><p>Monitoring keyword rankings and indexing health.</p></div>
      <div class="card"><h3>Meta Business Suite</h3><p>Tracking Instagram/Facebook ad performance and engagement.</p></div>
    </div>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 16. DIGITAL STRATEGY (master plan)
# ---------------------------------------------------------------
page(
    "digital-strategy.html", "DM Strategy", "The Complete Plan",
    'FULL DIGITAL <span class="accent">MARKETING STRATEGY</span>',
    "How every channel — SEO, SEM, social, email, content, and affiliate — works together toward one goal: membership growth.",
    """
<section>
  <div class="wrap">
    <h2 class="section-title">Objectives</h2>
    <div class="grid cols-3">
      <div class="card"><h3>Awareness</h3><p>Reach 50,000 local users per month through SEO, SEM, and social media.</p></div>
      <div class="card"><h3>Acquisition</h3><p>Convert 4% of website visitors into trial sign-ups.</p></div>
      <div class="card"><h3>Retention</h3><p>Improve 90-day member retention from 55% to 70% via email and community engagement.</p></div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <h2 class="section-title">Channel Funnel</h2>
    <div class="timeline">
      <div class="step"><h3>Top of Funnel — Awareness</h3><p>SEO blog content, YouTube tutorials, and Instagram reels attract new visitors.</p></div>
      <div class="step"><h3>Middle of Funnel — Consideration</h3><p>Google Ads and retargeting bring visitors back to the Membership page.</p></div>
      <div class="step"><h3>Bottom of Funnel — Conversion</h3><p>Free trial offer + email nurture sequence closes the sign-up.</p></div>
      <div class="step"><h3>Post-Conversion — Retention</h3><p>Referral program and community content keep members engaged long-term.</p></div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <h2 class="section-title">90-Day Roadmap</h2>
    <table>
      <tr><th>Phase</th><th>Focus</th><th>Key Actions</th></tr>
      <tr><td>Month 1</td><td>Foundation</td><td>Website SEO audit, Google Business Profile setup, content calendar launch</td></tr>
      <tr><td>Month 2</td><td>Paid Growth</td><td>Launch Google Ads + Instagram campaigns, referral program live</td></tr>
      <tr><td>Month 3</td><td>Optimize & Scale</td><td>Analyze GA4 data, double down on best-performing channels</td></tr>
    </table>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 17. FAQ
# ---------------------------------------------------------------
page(
    "faq.html", "FAQ", "Got Questions?",
    'FREQUENTLY ASKED <span class="accent">QUESTIONS</span>',
    "Everything you need to know before joining FlexFit.",
    """
<section>
  <div class="wrap" style="max-width:760px;">
    <details class="faq" open><summary>Do I need a membership to try a class?</summary><p>No — first-time visitors get one free trial class before choosing a plan.</p></details>
    <details class="faq"><summary>Can I freeze my membership?</summary><p>Yes, memberships can be paused for up to 30 days per year at no extra cost.</p></details>
    <details class="faq"><summary>Do you offer personal training separately?</summary><p>Yes, personal training sessions can be purchased individually or bundled into the Elite plan.</p></details>
    <details class="faq"><summary>Is there a joining fee?</summary><p>No joining fee — you only pay the monthly membership rate.</p></details>
    <details class="faq"><summary>How do I redeem a referral code?</summary><p>Enter the referral code at checkout on the Membership page or mention it at the front desk.</p></details>
  </div>
</section>
"""
)

# ---------------------------------------------------------------
# 18. CONTACT
# ---------------------------------------------------------------
page(
    "contact.html", "Contact", "Get In Touch",
    'CONTACT <span class="accent">US</span>',
    "Questions about membership, classes, or partnerships? Reach out.",
    """
<section>
  <div class="wrap grid cols-2">
    <div>
      <div class="form-field"><label>Name</label><input type="text" placeholder="Your full name"></div>
      <div class="form-field"><label>Email</label><input type="email" placeholder="you@example.com"></div>
      <div class="form-field"><label>Message</label><textarea rows="5" placeholder="How can we help?"></textarea></div>
      <button class="btn solid">Send Message</button>
    </div>
    <div class="card">
      <h3>Visit Us</h3>
      <p>123 Fitness Avenue, Your City, 400001</p>
      <h3 style="margin-top:20px;">Contact</h3>
      <p>hello@flexfitgym.com<br>+91 98765 43210</p>
      <h3 style="margin-top:20px;">Hours</h3>
      <p>Mon–Sat: 6 AM – 10 PM<br>Sunday: 8 AM – 6 PM</p>
    </div>
  </div>
</section>
"""
)

print("All 18 pages generated.")
