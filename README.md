Overview

This project is a gesture-controlled Rock–Paper–Scissors game powered by an adaptive Reinforcement Learning (RL) agent that learns how humans play.
It combines:

 MediaPipe for real-time hand gesture recognition

Interactive gameplay using OpenCV/Tkinter

 Q-learning + opponent modelling

Real-time performance graphs

Markov-style behaviour prediction

The AI does not play randomly — it actually studies your patterns, learns your habits, and improves after every round.

Inspired by concepts from behavioural game theory and opponent modelling research, this project demonstrates how AI can adapt to human behaviour in an interactive environment.

 Key Features

Real-time hand gesture recognition using MediaPipe (Rock / Paper / Scissors)

Adaptive Q-learning agent (learns from wins, losses, and your repeated patterns)

Five difficulty levels simulating the AI’s “growth” from beginner to expert

Opponent Modelling using:

Frequency analysis

Win-Stay / Lose-Shift behaviour

Markov chain sequence patterns

Live performance dashboard showing:

AI accuracy

Win rate

Learning progress

Interactive UI with OpenCV + Tkinter

 Tech Stack
Component	Technology
Hand Gesture Recognition-	MediaPipe Hands + OpenCV
Reinforcement Learning-	Q-learning with ε-greedy policy
Game Interface-	OpenCV + Tkinter
Pattern Modelling	Markov Chains, Frequency Tables
Real-Time Graph	Matplotlib
Language	Python 3
 How the AI Learns
1. Q-Learning

The AI updates a Q-table containing the “value” of choosing Rock, Paper, or Scissors in different states.

1. Reward system:

 Win → +1

 Tie → 0

 Loss → −1

2. ε-Greedy Strategy

To avoid becoming predictable:

With probability ε → explore (try a random action)

With probability 1−ε → exploit (choose best known action)

Difficulty Level 5 uses:

ε = 0.05  # 95% exploitation, 5% exploration

3. Markov-Style Opponent Modelling

The AI also tracks:

What you tend to play after winning

What you tend to play after losing

Your repeated move sequences

Your Rock/Paper/Scissors biases

This makes it behave more like a human-aware agent, not a random bot.

 Gesture Recognition Pipeline

MediaPipe detects 21 hand landmarks

A custom rule-based classifier identifies:

Rock (fist)

Paper (open palm)

Scissors (two fingers)

This approach is extremely fast and works better than CNNs for real-time play.
