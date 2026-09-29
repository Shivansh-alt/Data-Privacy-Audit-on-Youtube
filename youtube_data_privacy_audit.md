# Data Privacy Audit of YouTube

## 1. Introduction

YouTube is a video-sharing platform operated by Google. Because users interact with the platform through searches, video views, likes, comments, subscriptions, and other activities, YouTube processes a substantial amount of user and usage-related information.

This data privacy audit examines YouTube's privacy practices to identify potential privacy risks and evaluate the controls available to users. The audit focuses on **data collection, data use, personalization, advertising, data sharing, user controls, and privacy risks**.

> **Audit basis:** Publicly available Google/YouTube privacy documentation reviewed in September 2026. This is a desk-based privacy audit, not a technical penetration test or an independent security audit.

## 2. Objectives of the Audit

The main objectives are:

1. Identify the categories of information that YouTube/Google collects through YouTube.
2. Examine the purposes for which the information is used.
3. Examine how YouTube uses watch and search activity for personalization and recommendations.
4. Examine the relationship between YouTube activity and personalized advertising.
5. Identify potential privacy risks arising from these practices.
6. Examine the privacy controls available to users.
7. Provide recommendations for reducing privacy risks.

## 3. Scope

The audit covers:

- Google Account and YouTube-related information
- Search and watch history
- Interactions with videos, advertisements, and other content
- Device and technical information
- Personalization and recommendation systems
- Advertising and ad personalization
- Third-party services and integrations
- User access, deletion, and privacy controls
- General privacy and data-protection risks

The audit does not attempt to test YouTube's internal infrastructure, source code, encryption implementation, or incident-response systems.

## 4. Data Collection

Google's Privacy Policy applies to YouTube and describes information collected when users use Google services. Google states that activity information may include search terms, videos watched, interactions with content and advertisements, purchase activity, and activity on third-party sites and apps that use Google services. When users are signed in, information may be associated with their Google Account. [1]

YouTube also states that search and watch history can be used to improve recommendations and search results. Users can view or delete this history through YouTube's privacy controls. [2]

### Major categories of data

| Data category | Examples | Privacy relevance |
|---|---|---|
| Account information | Name, profile information and other Google Account information | Can directly or indirectly identify a user |
| YouTube activity | Videos watched, searches, interactions | Can reveal interests and behavioral patterns |
| Advertising interactions | Interactions with advertisements | Can contribute to advertising personalization |
| Device/technical information | Browser, device and related technical information | Can help provide and operate the service |
| Third-party activity | Activity on sites/apps that use Google services | Can extend the amount of information associated with a user's online activity |
| User-generated content | Comments and other content shared on YouTube | May be publicly visible depending on the feature and user's actions |

## 5. Purpose of Data Processing

According to YouTube, user data may be used to improve the YouTube experience, including remembering what a user has watched and providing more relevant recommendations and search results. YouTube also states that activity and information can be used to personalize advertisements within YouTube and other Google services. [2]

Google also states that it uses aggregated/anonymized YouTube data to improve services, including diagnostics, bug fixing, and performance improvements. [2]

Therefore, the main processing purposes identified in this audit are:

- Providing and operating YouTube
- Improving recommendations and search
- Personalizing the user experience
- Advertising and ad personalization
- Analytics and service improvement
- Security and service protection

## 6. Watch and Search History

Watch and search history are particularly important from a privacy perspective because they can reveal a user's interests and viewing behavior.

YouTube states that search and watch history can be used to improve recommendations and can also be used to show relevant and useful advertisements. Users can view, delete, or pause this history. [2]

### Privacy risk

A long-term history of searches and viewed videos may allow a detailed behavioral profile to be created. The sensitivity of such a profile depends on the nature of the content a person searches for or watches.

**Risk level: Medium–High**

**Mitigation/control:** Users can manage YouTube History and use deletion or auto-delete controls. [2]

## 7. Personalization and Recommendations

YouTube uses information about user activity to personalize experiences such as recommendations and search results. [2]

Personalization provides functional benefits, but it also means that a user's activity can influence the content presented to them.

### Privacy risk

Extensive behavioral data can create a detailed profile of a user's interests and preferences.

**Risk level: Medium**

**Mitigation/control:** Users can manage activity and personalization settings through Google Account and YouTube privacy controls. [2][3]

## 8. Advertising and Data Use

YouTube states that advertisements can be personalized using factors such as Google Account information, activity on Google services, websites visited, mobile app activity, information from partners, and YouTube interactions. [4]

Google's My Ad Center allows users to control whether information and activity associated with their Google Account are used to personalize ads. Users can also control the use of YouTube History for ad personalization. [3]

### Privacy risk

The combination of activity and advertising information can increase the amount of behavioral profiling associated with a user.

**Risk level: High**

**Mitigation/control:** Users can turn personalized advertising off and manage specific information used for ad personalization through My Ad Center. [3]

## 9. Data Sharing and Third Parties

Google's Privacy Policy describes circumstances in which information may be disclosed, including when users choose to share information, to third parties with user consent, to service providers processing information on Google's behalf, and where required for legal reasons. [1]

Google also provides controls for reviewing third-party applications and sites that have access to Google Account data. [1]

### Privacy risk

Third-party integrations can increase the number of organizations or systems involved in processing user-related information.

**Risk level: Medium**

**Mitigation/control:** Review and revoke unnecessary third-party application access through Google Account controls.

## 10. User Privacy Controls

YouTube and Google provide several controls that allow users to manage their data.

Important controls include:

- View, delete, or pause YouTube Watch History
- View, delete, or manage YouTube Search History
- Automatic deletion/auto-delete options
- Google My Activity
- Google Privacy Checkup
- My Ad Center
- Controls for YouTube History used for advertising
- Google Account security controls such as 2-Step Verification

Google states that users can use My Activity to view and control saved activity and can use Privacy Checkup to review important privacy settings. [3]

## 11. Privacy Risk Assessment

| Risk | Description | Likelihood | Impact | Overall risk |
|---|---|---:|---:|---:|
| Behavioral profiling | Search/watch activity can contribute to personalized experiences and advertising | Medium | High | High |
| Exposure of viewing history | Viewing and search history may reveal personal interests if improperly accessed | Medium | High | High |
| Extensive data collection | Multiple categories of activity and technical information may be processed | Medium | High | High |
| Third-party access | Third-party integrations can involve additional data processing | Medium | Medium | Medium |
| Uncontrolled personalization | Users may not fully understand which activity affects personalization | Medium | Medium | Medium |
| Account compromise | Unauthorized access to a Google Account could expose associated YouTube activity | Medium | High | High |

**Note:** The risk ratings above are an academic assessment based on the potential privacy impact of the practices described in public documentation. They are not a finding that YouTube has experienced a particular security failure.

## 12. Audit Findings

### Finding 1: Significant behavioral data is processed

YouTube processes activity such as searches, videos watched, and interactions. This data can be used to personalize recommendations and other experiences. [1][2]

**Privacy concern:** Such information can reveal detailed patterns about a user's interests.

### Finding 2: YouTube activity can be relevant to advertising

YouTube and Google provide controls concerning the use of YouTube History and other activity for personalized advertising. [3][4]

**Privacy concern:** Advertising personalization can involve multiple categories of activity and information.

### Finding 3: Users have substantial privacy controls

Users can view, delete, or pause YouTube history and manage advertising personalization. Google also provides My Activity and Privacy Checkup. [2][3]

**Privacy concern:** The existence of controls does not eliminate the need for users to understand what each setting controls.

### Finding 4: Third-party integrations require attention

Google's policy describes disclosure to third parties in specified circumstances and provides controls for managing third-party access to Google Account data. [1]

**Privacy concern:** Users should periodically review connected third-party applications and remove unnecessary access.

## 13. Recommendations

Based on the audit, the following measures are recommended:

1. **Data minimization:** Collect and retain only the information necessary for the stated purpose.
2. **Clear privacy explanations:** Explain in simple language how watch and search activity affects recommendations and advertising.
3. **Privacy-by-default options:** Provide strong privacy choices that are easy for users to understand.
4. **Easy history management:** Make deletion, pausing, and auto-delete controls easy to locate.
5. **Third-party access review:** Encourage users to regularly review connected applications and revoke unnecessary access.
6. **Stronger account protection:** Encourage the use of 2-Step Verification and other account-security measures.
7. **Transparency about personalization:** Clearly distinguish data used for recommendations from data used for advertising.
8. **Regular privacy reviews:** Periodically reassess data collection and retention practices as features and regulations change.

## 14. Conclusion

The audit shows that YouTube's service depends on processing significant amounts of user activity and related information. Search history, watch history, interactions, and other information can support recommendations, personalization, advertising, and service improvement.

At the same time, YouTube and Google provide users with controls for reviewing, deleting, and managing activity and advertising personalization. The principal privacy risks identified in this academic audit concern **behavioral profiling, exposure of viewing history, extensive data processing, third-party access, and account compromise**.

Overall, effective privacy protection requires both organizational safeguards and informed use of the privacy controls provided to users.

## 15. References

1. Google Privacy Policy, effective May 26, 2026:  
   https://policies.google.com/privacy

2. YouTube Help — Understanding the basics of privacy on YouTube apps:  
   https://support.google.com/youtube/answer/10364219

3. Google My Ad Center Help — Control what data Google uses to show you ads:  
   https://support.google.com/My-Ad-Center-Help/answer/12156161

4. YouTube Help — Manage what types of ads you see on YouTube videos:  
   https://support.google.com/youtube/answer/7403255

5. Google Account Help — How Google protects your privacy and keeps you in control:  
   https://support.google.com/accounts/answer/10400210

---

**Project title:** Data Privacy Audit of YouTube  
**Audit type:** Desk-based privacy audit  
**Review period:** September 2026
