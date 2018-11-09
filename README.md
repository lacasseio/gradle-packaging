# Gradle Packaging Support
## Problem
Officially, the Gradle team has only the bandwidth to package Gradle distribution as a zip hosted on [their Website](https://gradle.org/install/). The Gradle community is strong and filled with motivated developers to maintain a varity of packaging support such as Debian, Fedora, Homebrew, MacPorts, etc. The fundamental issue with this approach is the transparency of the process used to publish those package. As an user, you are trusting those adhoc process. After looking at some of them, I'm seeing horrors such as patching the distribution to use a different dependency version then what was originally build with. Although those patch were probably done with care, it deliver a similar but different version of Gradle to the consumer. These difference is what could cause a bad experience Gradle and in turn hurt Gradle's reputation. It goes without saying that some of these adhoc process could fall out of date due to the unavailibility of the maintainer or, worst, packaged with unsafe code.

## Solution
Let's gather all the Gradle packaging support in the same repository and automate everything under the same, transparent, process. The goal is to be greatful to all their hard work done by the maintainer and centralizing all the packaging support needs of the community. On the security side, we can vet that the distribution remains intact throughout the packaging chain.

## Contribution
We accept all contribution regarding how each packaging needs to be supported. Each packaging support automation chain needs to include test coverage.
