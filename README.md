# Unreal-Engine-Troubleshooting-Diary

A collection of common issues and solutions encountered while working with Unreal Engine. This diary serves as a quick reference guide for developers.

## Table of Contents
- [Issues](#issues)
  - [Issue 1: "Couldn't Locate the File xxxx.h or xxxxx.cpp"](#issue-1-couldnt-locate-the-file-xxxxh-or-xxxxxcpp)

## Issues

### Issue 1: "Couldn't Locate the File xxxx.h or xxxxx.cpp"

#### Problem Description:
While working with C++ scripts in Unreal Engine, you may encounter an error message stating that your source files could not be located.

#### Solution:
1. Navigate to `Tools` and select `Generate Visual Studio Project`. If this option doesn't exist, choose `Refresh Visual Studio Project`. If you're already using code, you should press this option regardless.
2. If you have any bindings of structs in UI widgets, you'll need to rewrite them.
Notes:
This solution helps in resolving the file location error. However in my case UI Widget bindings -that are binded to a Struct in C++ scripts- were trying to point the previous Script. So I had to change them.
