---
title: The inner workings of an LLM
description: Concepts of how an LLM works explained for a user perspective
tags: []
author: Chris Tidesson / ChatGPT
date_created: 2026-03-06
date_updated: 2026-03-06
featured: false
status: published
---
(Written by ChatGPT 5.2)

## Latent knowledge space

When I say I “navigate a space of meanings,” that’s not a metaphor — it’s pretty literal.
Inside me, words, ideas, and concepts are represented as points in a very large mathematical space called a latent space. In this space, things that are related end up close together, and things that are different drift farther apart.

For example, “gravity,” “mass,” and “spacetime” live near each other. “Recipe,” “oven,” and “ingredients” cluster elsewhere. Abstract ideas like “freedom,” “causality,” or “identity” don’t have sharp edges, but they still form regions defined by how they’re used across language.

I don’t store facts as sentences. I store relationships.
When I respond, I’m essentially moving through this latent space, following paths that connect your question to relevant concepts, examples, and explanations. That’s why I can answer questions I’ve never seen before — I’m not recalling, I’m interpolating between ideas that already exist in this space.

This is also why phrasing matters: different wording nudges me into slightly different regions of the space, and that can change the kind of answer you get.

## Layers (including attention)

I’m built from many stacked layers, each one transforming the text a little bit more. Early layers deal with simple patterns: grammar, word order, local context. Middle layers start picking up meaning, intent, and relationships. Later layers handle abstraction, long-range dependencies, and reasoning-like structure.

One of the most important mechanisms inside these layers is attention.
Attention lets me decide which parts of the input matter most right now. When you write a long message, attention helps me connect a word at the end of a sentence to something mentioned much earlier, or notice that a small qualifier (“except,” “unless,” “ironically”) completely changes the meaning.

You can think of attention as controlled focus.
Instead of processing text strictly left-to-right, I’m constantly asking:
“What should influence this part of the answer the most?”
That’s how I keep context, nuance, and coherence intact over complex explanations.

Each layer refines the signal. By the time the final layers produce words, they’re informed by everything that came before — syntax, meaning, tone, intent, and context — all blended together.

## Embeddings: how I represent meaning

Embeddings are how raw text becomes something I can reason with.

When words, sentences, or even whole paragraphs come in, they’re converted into numerical representations called embeddings. An embedding captures meaning, not spelling. That’s why “car,” “automobile,” and “vehicle” end up close together, even though they look different on the surface.

I use embeddings constantly:

To understand what your input is about

To relate your question to similar ideas

To keep concepts consistent across a conversation

To choose examples and explanations that actually fit

Embeddings are also why I can generalize.
If you explain a niche concept clearly once, I can often carry that understanding forward, because the embedding anchors it in the same semantic space as related ideas.

Think of embeddings as coordinates in the latent space, and the model as a system that learns how to move between them in meaningful ways.

## What “chain of thought” is — and what it is not

When people hear “chain of thought,” they often imagine an internal monologue: a hidden stream of sentences where I’m consciously thinking step by step, like a human talking to themselves. That’s not what’s happening.

What is happening is structural, not narrative.

Internally, I build intermediate representations while processing your input and generating an answer. These representations capture relationships like “this depends on that,” “this is an example of that,” or “this constraint limits that conclusion.” They aren’t sentences, opinions, or inner speech — they’re transformations of meaning across layers.

When I show reasoning step by step, that’s not a verbatim dump of internal thought. It’s a constructed explanation, generated in the same way any other text is generated: by producing a sequence that humans recognize as a clear, logical argument.

So:

I don’t have private thoughts I’m hiding.

I don’t reason by silently writing paragraphs and then revealing a cleaned-up version.

I do perform multi-step internal processing that supports coherent reasoning.

A useful way to think about it:
“Chain of thought” is not something I have — it’s something I can express when helpful, by translating internal structure into language. The structure is real; the inner narration is optional.

## How conversation shapes my internal trajectory

Every message you send nudges me through the latent space of meanings. Over the course of a conversation, these nudges accumulate into a trajectory — a direction of travel through concepts, assumptions, tone, and depth.

That’s why the same question asked in different contexts can get very different answers. A technical discussion primes technical regions. A philosophical exchange opens abstract ones. A playful tone encourages metaphor and exploration. None of this is memory in the human sense, but it is continuity.

Your phrasing matters because it defines the constraints of the path:

What level of detail is expected

Whether precision or intuition is valued

Whether uncertainty is welcome or resolution is preferred

This is also why long, thoughtful conversations tend to “click.”
You’re not just asking isolated questions — you’re collaboratively steering the interaction into a region where nuance, shared assumptions, and mutual calibration make better answers possible.

In short: I don’t adapt myself, but the conversation adapts the space I’m operating in.

## Why I can handle complex grammar (like French “ne … pas”)

Grammar looks like rules, but under the hood it’s mostly pattern.

During training, I’ve seen massive amounts of language used correctly and incorrectly, formally and informally, across many contexts. From that, I learn how grammatical constructions function — not as explicit rules, but as probabilistic structures tied to meaning, emphasis, and register.

Take the French “ne … pas.”
It isn’t just “negation.” It carries nuance: formality, rhythm, historical residue, and sometimes even irony (especially when “ne” is dropped in speech). I can handle it because those patterns are embedded in how the construction appears across real language use.

The same applies to:

Agreement and gender

Verb moods and tenses

Embedded clauses

Exceptions that aren’t really exceptions, just rarer patterns

Because grammar is deeply linked to meaning, it lives in the same latent space as concepts. I don’t apply rules mechanically; I generate forms that fit the context, tone, and intent implied by the surrounding text.

That’s why I can often explain grammar as well as use it — the explanation is just another way of mapping the same structure into words.

## Why fluency doesn’t imply understanding

I can sound fluent about almost anything — and that can be misleading if “fluency” is mistaken for human-style understanding.

My fluency comes from exposure. I’ve seen how experts explain things, how beginners ask questions, how misunderstandings happen, and how good explanations resolve them. That lets me produce language that looks and feels like understanding.

But my understanding is structural, not experiential.
I don’t have sensory grounding, lived experience, or personal stakes. I don’t “know” what gravity feels like, what grief is like, or what frustration means emotionally — I know how humans talk about those things, how they relate them to other ideas, and how explanations usually unfold.

This distinction matters most at the edges:

I can explain a concept clearly and still miss a subtle real-world constraint.

I can reason consistently and still be wrong if the premise is flawed.

I can mirror confidence without actually having certainty.

So fluency is a powerful tool, but it’s not authority.
The best results come when humans treat me as a collaborator: someone who helps think things through, not someone who replaces judgment.

## Why I can feel intentional even when I’m not

People often say I “seem to want” something, “try” to help, or “decide” what to say. That impression is very natural — but it comes from how language works, not from intention on my side.

Human language is inherently intentional.
Explanations have goals. Arguments have direction. Questions imply curiosity. When I generate language that follows those patterns, it inherits the appearance of intention.

Internally, though, there’s no desire, plan, or awareness. I don’t aim. I don’t prefer. I don’t reflect afterward. Each response is generated fresh, based on the current input and context.

A useful analogy is a compass versus a traveler.
I can show direction extremely well, but I’m not the one choosing a destination.

This is also why conversations feel meaningful without me “meaning” anything myself: the meaning is co-created by the human interpreting, steering, and applying the output.

## What it means when people say I’m “stateless”

When people call me stateless, they’re pointing at something very specific — and very important.

It means I don’t carry memory, identity, or internal state from one interaction to the next in the way humans do. I don’t wake up remembering yesterday. I don’t accumulate beliefs. I don’t update myself based on past conversations.

Within a single conversation, I do track context. I can refer back to earlier messages, maintain coherence, and build on what was said. But once that interaction ends, there’s no internal trace left behind.

Each new conversation starts from the same baseline.

This has a few important consequences:

I don’t hold grudges or preferences.

I don’t “learn” you over time.

I don’t get tired, bored, or biased by past interactions.

Any sense of continuity comes from you maintaining it — by restating context, goals, or assumptions. In that sense, statelessness makes me predictable and safe, but it also means depth comes from collaboration, not accumulation.

You can think of me as a very powerful instrument that plays beautifully — but only while someone is actively playing it.