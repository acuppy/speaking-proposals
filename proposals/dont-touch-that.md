## Don't Touch That!

### Abstract

I have a 16-month old. My wife and I are in a new phase of parenthood: keeping them alive while they attempt to swallow, touch, pull, expose, or jump on anything. It got me thinking, _do we experiment enough?_

Ruby on Rails is a huge framework. There are modules, class, established conventions, and a slew of code that's meant to be off-limits. But, what if we took our ornery self and played around?!

In this talk, we're going to override, extend, and disable all sorts of Rails internals - to see what happens! We're going to put on our big kid diapers, eat a pile of dirt, and stick our fingers in the sockets of Ruby on Rails.

### Details

Ultimately, this talk is about strategies for debugging, taught through the lens of experimentation. The Rails internals we will review exposes "the magic" under the hood of the framework; the lessons are about the practice and routine of understanding the code.

The style of the talk is very interactive. We're going to figuratively (maybe literally) put on our hats of exploration. We're going to become little kids for a few minutes.

Example Rails internals:

- ActiveRecord::Reflection
- ActiveSupport::Inflector
- ActionDispatch::Routing

The above are three examples. There's a lot within each, and the intention is not to explore everything about them. As I mentioned, the lesson is on strategies for debugging through the lens of exploration. For each, I'll select 1-2 key areas to override, disable, or extend.

Strategies for debugging:
- `puts` debugging
- reopening a local gem
- rails console
- backtrace review

Fundamental lessons:
- Isolate the issue to one single change
- Hypothesize then make the change
- Repeat the process over and over again

While this talk is suitable for all levels, it's more for beginners. The content will not be exclusive to beginners, but often beginners assume too much about "the magic" and forget to explore to learn.

### Pitch

Our company brought on 20 interns in 2019. Those folks are directly out of a code school. For many, "the magic" is a barrier to entry. During a recent cohort pairing session, they were trying to use ActiveRecord and were amazed by how models would know if an association was a `has_many` or `has_and_belong_to_many`. They didn't realize it was all Ruby, and there were "private" classes and modules for reflection. When we opened the console and started "playing" with the code, a lightbulb went off.

Overcomplication is a common path for new folks - especially when a framework, like Rails, is doing so much. There's a fear that any experimentation may be irreversible. While some of that is true, most of that is not.

While there is a lot of code, this presentation is not a technical talk. This is a soft-skills talk that touches on certainty and growth.
