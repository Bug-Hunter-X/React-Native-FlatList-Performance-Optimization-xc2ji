# React Native FlatList Performance Optimization

This repository demonstrates a common performance issue in React Native's `FlatList` component when dealing with large datasets and provides a solution using optimized rendering techniques.

## Problem

When rendering a `FlatList` with thousands of items, the app may become sluggish due to inefficient rendering of all items regardless of visibility.  Scrolling can become jerky and unresponsive.

## Solution

The solution uses the `windowSize` prop of `FlatList` and potentially further optimization with libraries like `react-native-fast-image` for improved image handling, if your dataset includes images. By setting `windowSize` to a small number, you control the number of items rendered at any given time, only rendering what's visible and nearby items.  This significantly improves performance.