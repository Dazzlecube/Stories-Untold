---
title: Artifical vs Biological Neurons 
date: 2023-12-11
description: "Brain biology and organization is complex. Some of this complexity is not captured in our current artificial neural networks, which could limit their potential."
tags:
   - extraordinaryphysics
---

Our current Artificial Neural Networks (ANN) are 'biologically-inspired'.
Similar to our brain, they comprise a series of neuron-like units that can be active or not depending on their inputs.
They are connected in multiple layers with different weights, mimicking some of our brain's organization and synaptic connections. 
And with access to more computing power than ever, ANNs now power multiple advanced applications, from regression analysis to classification or robotics. 

The success of these networks, however, make people forget that they look very different than our brain. 
And brains are very different than current ANNs. For example: 
- Organization: Our brain features strong feedback loops rather than the feedforward connections found in ANNs. 
- Connections: Neurons receive numerous inputs (typically in the range of 100-1000 per neuron) as opposed to the sparse patterns (5-10 per neuron) used in ANNs 
- Energy consumption: Our brains are very efficient, consuming ~20 W, while a typical GPU will consume >200 W 

And there are many more differences. Synapses' activation is unreliable, and their intensity changes depending on their stimulation patterns, creating neuro-plasticity for learning. Even glial cells - which are non-spiking cells in between neurons - are increasingly recognized to play a computational role in the brain.

So that brain looks very different than our artificial networks. 
Does it matter? 

It is conceivable that all computational problems could one day be solved using variants of our current ANN architecture together with (lots of) computing power. 
Even if that turns out to be the case, I'm willing to bet that this will be highly inefficient to do so. 
Using more biologically realistic networks could accelerate or provide efficient alternatives, even tough they are more complex to understand and simulate. 

Exploring the differences between real and artificial neural networks could become a whole book in itself, so in this post I'll focus on one specific difference, namely how biological *neurons* differ from the artificial neurons used in ANNs. 
Indeed, most if not all computer scientists I talk to genuinely think that neurons behave like '0' or '1' units (1 corresponding to a spike) without any additional complexity. 

To model neurons computer scientists use a so-called 'activation function', which measures how a neuron reacts based on the inputs it receives. In many cases the activation function is very simple, i.e. sum all incoming inputs to the neuron, and if it's higher than a given threshold the neuron activates (1), otherwise it stays silent (0). Others use slightly more sophisticated activation functions such as sigmoid functions, but it essentially has the same effect. 

Real neurons do spike, i.e. emit a brief action potential that is then propagated along the axon and eventually triggers (or not) a synapse. But the dynamics is very different.

The simplest and most compelling way I know to illustrate this comes from the work of Izhikevich. 
Izhikevich introduced a simplified set of two-variables equations to simulate spiking neurons more efficiently than a full dynamical description. [^1]
When simulating neurons with constant or short pulses of current, what you observe is completely different than the simple spike-or-not-spike behavior assumed in artifical neurons: 

{{< figure src="neurondynamics.png" caption="*Neuronal dynamics observed for simple current stimulations. Electronic version of the figure and reproduction permissions are freely available at www.izhikevich.com*" >}}

<br>

This diversity of behavior is stunning (and the fact that this can be reproduced with a simple 2-dimensional system is even more unexpected). Even negative currents can trigger spikes!

Importantly, these behaviors are not theoretical artifacts: neurons with these spiking patterns are observed in the brain. 
What's more, these different spiking patterns play essential biological and computational roles. 
Bursts or frequency adaptation, for instance, directly influence the probability of synapses being activated and thus learning mechanisms.

These neuronal dynamics adds a layer of complexity to understanding the brain, especially when combined together to form a recurrent network. 
Nonetheless, the fact that our brain uses different types of neurons with different dynamical properties suggests that this complexity might be worth it when solving real-life tasks efficiently. 

<br>

[^1]: Neurons are typically described by multiple non-linear equations. Key variables include the membrane voltage and the conductance of the various ion channels. 
