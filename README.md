# React Native Dimensions API: Initial Render Issue

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native. The problem arises because the dimensions are not immediately available when the component first renders, leading to unexpected layout behavior or potential crashes.  The solution provides a robust approach using the `useEffect` hook to obtain accurate dimensions.

## Problem

The `Dimensions` API in React Native provides screen width and height. However, if you access these values during the initial render, you might get incorrect or undefined values, causing layout problems.

## Solution

The solution uses the `useEffect` hook to ensure the dimensions are obtained after the component has fully mounted. The `Dimensions.addEventListener` ensures that if the screen dimensions change (e.g., device rotation), the component re-renders with the updated values.