---
layout: default
title: Microsoft Defender for Cloud
---

{% include navigation.html %}
{% include breadcrumb.html %}

# 🛡️ Microsoft Defender for Cloud

**Organization:** Prafydob Corp
**Duration:** 30 minutes
**Environment:** Microsoft Azure
**Status:** ✅ Completed

---

## 📋 Overview

Prafydob Corp's Azure infrastructure needed more than network controls.
The virtual machines running business operations required active
protection against threats that network rules alone cannot stop.
This implementation activated Microsoft Defender for Cloud Plan 2
at the subscription level, providing enterprise-grade threat
protection across all current and future virtual machines
without requiring infrastructure changes.

---

## 🎯 Objectives

- Enable Microsoft Defender for Cloud enhanced security features
- Activate Defender for Servers Plan 2 at subscription level
- Establish continuous vulnerability assessment
- Enable Just-in-Time VM access to reduce attack surface
- Verify active monitoring through the recommendations interface

---

## 🔐 Why This Matters for Prafydob Corp

Prafydob Corp processes customer transactions and handles sensitive
data as an e-commerce business. A network firewall controls
traffic in and out but cannot detect threats already inside
the environment. Microsoft Defender for Cloud fills this gap
by continuously monitoring server behavior, scanning for
vulnerabilities, and alerting on suspicious activity. This
moves Prafydob Corp from reactive to proactive security.

---

## 🏗️ Security Architecture Context

This implementation sits on top of the existing network security
controls established in previous labs.
Azure Subscription (Prafydob Corp)
│
├── Network Layer (Azure Firewall - Lab 03)
│     └── Controls what traffic enters and exits
│
└── Threat Protection Layer (Defender for Cloud - This Lab)
└── Monitors what happens inside the environment
├── Threat Detection
├── Vulnerability Assessment
├── Just-in-Time VM Access
└── File Integrity Monitoring
---

## 🔧 Implementation Steps

### Phase 1: Accessing Microsoft Defender for Cloud

Microsoft Defender for Cloud was accessed through the Azure
Portal search bar. The overview page displayed the current
security posture dashboard, giving initial visibility into
the subscription's security status.

**[INSERT SCREENSHOT 1: Microsoft Defender for Cloud overview page]**
*Caption: Defender for Cloud overview showing current security posture*

---

### Phase 2: Environment Settings Configuration

The Management section was accessed through the left navigation
sidebar. Environment settings was selected to reach
subscription-level configurations. The settings page displayed
a hierarchical structure representing the Azure tenant. The
subscription node was expanded to reveal all available
Defender plan configurations.

**[INSERT SCREENSHOT 2: Environment settings showing subscription hierarchy]**
*Caption: Environment settings displaying tenant and subscription structure*

---

### Phase 3: Activating Defender for Servers Plan 2

Within the Defender plans interface the Servers plan was
identified in the Cloud Workload Protection list showing
a status of Off. This confirmed that enhanced server
protection was not yet active for the subscription.

**[INSERT SCREENSHOT 3: Defender plans showing Servers status as Off]**
*Caption: Servers plan in Off state prior to activation*

The Servers plan was toggled from Off to On. The system
automatically configured Plan 2, the most comprehensive
protection tier available. Plan 2 was selected because it
includes advanced capabilities that Plan 1 does not offer.

**[INSERT SCREENSHOT 4: Plan 2 selected and features displayed]**
*Caption: Defender for Servers Plan 2 selected with full feature set*

The configuration was saved using the Save button at the
top of the settings page. A success notification confirmed
the Defender plans were updated successfully.

**[INSERT SCREENSHOT 5: Save confirmation notification]**
*Caption: Success notification confirming Defender plans updated*

---

### Phase 4: Verifying the Deployment

The Servers plan entry was checked to confirm the status
change. The interface now showed the Servers plan as On
with Plan 2 clearly indicated.

**[INSERT SCREENSHOT 6: Servers plan showing On status with Plan 2]**
*Caption: Servers plan active with Plan 2 enabled*

The Recommendations blade was accessed to observe the
security features working. The JumpHostVM and WorkloadVM
from the Azure Firewall implementation appeared immediately
with associated risk factors and improvement opportunities.
This confirmed Defender for Cloud was actively monitoring
the infrastructure.

**[INSERT SCREENSHOT 7: Recommendations page showing VM risk assessments]**
*Caption: Active recommendations for JumpHostVM and WorkloadVM*

---

## 🔒 Security Capabilities Enabled

### Threat Detection and Behavioural Analytics
Defender for Cloud continuously analyses server behaviour
looking for unusual patterns. This includes unusual login
attempts, suspicious process creation, and potential malware
activity. The detection engine uses Microsoft's global threat
intelligence to identify known attack patterns.

### Vulnerability Assessment
Virtual machines are automatically scanned for security
weaknesses including missing patches, outdated software,
and misconfigurations. The assessment engine prioritises
findings so the most critical vulnerabilities are addressed
first.

### Just-in-Time VM Access
Management ports are kept closed by default. When
administrative access is needed, a time-limited request
opens only the required port for a specific IP address.
The port closes automatically when the time window expires.
This eliminates the constant exposure of management ports
to the internet.

### File Integrity Monitoring
Critical system files and registry keys are continuously
monitored for changes. Any unauthorised modification
generates an alert. This is particularly effective at
detecting threats that attempt to establish persistence
by modifying system files.

### Adaptive Application Controls
The system observes which applications run legitimately in
the environment and creates policies to block anything
outside that approved list. This provides protection
against malicious software attempting to execute on
protected servers.

### Security Posture Management
The Secure Score metric measures overall security health
across the subscription. Recommendations are automatically
generated and prioritised, giving the security team a
clear action list for improving Prafydob Corp's security
posture over time.

---

## 📊 Results and Validation

| Capability | Status | Verification Method |
|------------|--------|-------------------|
| Threat Detection | ✅ Active | Overview dashboard |
| Vulnerability Assessment | ✅ Active | Recommendations blade |
| Just-in-Time VM Access | ✅ Active | VM configuration page |
| File Integrity Monitoring | ✅ Active | Plan 2 feature list |
| Adaptive Application Controls | ✅ Active | Plan 2 feature list |
| Security Posture Management | ✅ Active | Secure Score displayed |

**Verification Outcome:** Both JumpHostVM and WorkloadVM
appeared in the Recommendations interface with active
risk assessments. This confirmed Defender for Cloud was
monitoring workloads and performing continuous security
assessments within minutes of activation.

---

## 💡 Key Learnings

### Subscription-Level Activation is Powerful
Activating at the subscription level means every new
virtual machine added to Prafydob Corp's environment
automatically receives protection. There is no risk of
new resources being deployed without monitoring.

### Complementary to Network Controls
Azure Firewall from Lab 03 controls traffic between
the network and the internet. Defender for Cloud monitors
activity within the virtual machines themselves. These
two controls together create much stronger protection than
either one alone. A threat that bypasses network rules
will still be detected by Defender for Cloud's behavioral
monitoring.

### Proactive Over Reactive
The recommendations interface gave an immediate list of
security improvements with clear priority levels. This
shifts the team from responding to incidents after they
happen to addressing weaknesses before attackers can
exploit them.

---

## 🔗 Related Projects

- [Azure Firewall Implementation](../azure-firewall-implementation/)
- [Cloud Security Overview](../)
- [Home](../../)

---

{% include page-nav.html %}

<a href="#" class="back-to-top">↑</a>
