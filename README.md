# 🌦️ Travel Weather Planner

A smart Python project that helps users decide whether they can travel based on **distance**, **weather conditions**, and **available transport options**.

---

## 🚀 Features

- 📍 Checks travel feasibility based on distance
- 🌧️ Considers weather conditions (rain/no rain)
- 🚲 Uses bike availability for short distances
- 🚗 Uses car or ride-share apps for long distances
- ⚡ Simple decision-making system using if-elif-else

---

## 🧠 Logic Used

### 1. If distance is 0 or falsy:
- Output: `False`

### 2. If distance ≤ 1 mile:
- `True` only if it is NOT raining

### 3. If distance is between 1 and 6 miles:
- `True` only if user has a bike AND it is NOT raining

### 4. If distance > 6 miles:
- `True` if user has a car OR ride-share app

---

## 💻 Code Example

```python
distance_mi = 7
is_raining = True
has_bike = True
has_car = False
has_ride_share_app = False

if not distance_mi:
    print(False)

elif distance_mi <= 1:
    if not is_raining:
        print(True)
    else:
        print(False)

elif distance_mi <= 6:
    if has_bike and not is_raining:
        print(True)
    else:
        print(False)

else:
    if has_car or has_ride_share_app:
        print(True)
    else:
        print(False)
