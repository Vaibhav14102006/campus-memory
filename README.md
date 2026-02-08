# Event Guidance System - Learn from Past Mistakes 🎓

## 🎯 What This System Does

When a student **registers for an event**, the system analyzes **past feedback from 100,000 records** and provides:

✓ **Common Issues** - What problems previous students faced  
✓ **Actionable Recommendations** - Specific advice to avoid mistakes  
✓ **Success Tips** - Learn from top performers  
✓ **Preparation Checklist** - What to bring and prepare  
✓ **Realistic Expectations** - What to expect based on past data  

---

## 📊 Example Output

### Student registers for: **Hacksetu (Hackathon)**

```
⚠️ COMMON ISSUES (from 9,046 past attendees):
  • Poor Coordination (19.4% reported)
  • Technical Issues (19.1% reported)  
  • Prize Delay (13.0% reported)

🔴 AREAS OF CONCERN:
  • Organization: 5.73/10
  • Content Quality: 5.73/10
  • Food Quality: 6.52/10

💡 RECOMMENDATIONS:
  🔥 [High Priority] Team Formation
     Teams of 5 had highest satisfaction. Form your team NOW!
  
  🔥 [High Priority] Technical Setup
     Bring backup chargers, power banks, essential equipment
  
  🔥 [High Priority] Arrive Early
     Coordination issues common. Keep emergency contacts handy

🏆 SUCCESS TIPS (from winners):
  1. 80% successful participants came with teams. Teamwork is key!
  2. Prize winners averaged 8.6/10 learning outcome. Focus on learning!
  3. Participate actively in all sessions

✓ PREPARATION CHECKLIST:
  □ Laptop & Charger (fully charged)
  □ Power Bank
  □ Team Formation complete
  □ 2-3 Project Ideas ready
  □ Snacks & Water
  □ Emergency Contacts saved
```

---

## 🚀 Quick Start

### Run the System:
```bash
python event_guidance_system.py
```

### Use the API:
```python
from event_guidance_api import get_event_guidance

student = {
    'branch': 'CSE',
    'year': 2,
    'skill_level': 'Intermediate',
    'gender': 'Male'
}

guidance = get_event_guidance(student, 'Hacksetu')

print(f"Expected Satisfaction: {guidance['overall_satisfaction']:.2f}/10")
print(f"Common Issues: {len(guidance['common_issues'])}")
for rec in guidance['recommendations']:
    print(f"• {rec['advice']}")
```

---

## 📁 Key Files

| File | Purpose |
|------|---------|
| **event_guidance_system.py** | Core system - analyzes feedback & generates guidance |
| **event_guidance_api.py** | Simple API with usage examples |
| **generate_dataset.py** | Generates 100K feedback records |
| **event_feedback_dataset.csv** | Historical data (100K records) |

---

## 💡 Real-World Integration

### Registration Page:
```python
# When student registers
guidance = get_event_guidance(student, event_name)

# Show popup with top 3 recommendations
show_popup(guidance['recommendations'][:3])
```

### Pre-Event Email (1 week before):
```python
send_email(
    to=student.email,
    subject=f"Tips for {event_name}",
    body=format_guidance(guidance)
)
```

---

## 📈 Sample Insights (100K Records)

### Best Events:
- **Ami Chroma**: 7.59/10, 78% recommendation
- **Convocation**: 7.58/10, 78% recommendation

### Challenging Events:
- **Smart India Hackathon**: 5.81/10, 28% recommendation
  - Issues: Technical (18%), Coordination (17%)

### Most Common Issues Overall:
1. Technical Issues (22%)
2. Poor Coordination (22%)
3. Prize Delay (9%)

### Success Factors:
- Content Quality: 9.34/10
- Organization: 9.31/10
- Networking: 8.44/10

---

## 🎯 Benefits

**Students:**
- ✅ Know what to expect
- ✅ Avoid common mistakes  
- ✅ Come prepared
- ✅ Higher success rate

**Organizers:**
- ✅ Identify improvement areas
- ✅ Reduce complaints
- ✅ Data-driven decisions

---

## 🔧 Requirements

```bash
pip install pandas numpy
```

---

## 📱 Available Events

- Hacksetu (National Hackathon)
- Anveshan (University Hackathon)
- Ami Chroma (Cultural)
- Smart India Hackathon
- Init Maths (Training)
- Convocation (Ceremony)
- Code Sprint, Tech Fest, Workshop AI/ML, Project Expo, Gaming Tournament

---

**Helping students succeed by learning from past experiences! 🎉**
