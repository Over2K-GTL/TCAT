# Blueprint API Reference

The **TCAT (Tactical Crowd AI Toolkit)** Blueprint API provides asynchronous, batched spatial queries for influence maps. These nodes allow agents to find optimal positions, evaluate threats, or analyze terrain without stalling the Game Thread.

---

## Class: `UTCATAsyncSearchAction`
*Base class for single-result asynchronous queries.*

### Functions

#### **Search Highest Value**
Asynchronously searches for the highest influence value within a specified radius. Useful for finding the "best" tactical position.

**C++ Syntax:**
```cpp
static UTCATAsyncSearchAction* SearchHighestValue(
    UObject* WorldContextObject,
    FName MapTag,
    FVector SearchCenter,
    float SearchRadius,
    bool bExcludeUnreachableLocation,
    bool bTraceVisibility,
    bool bIgnoreZValue,
    UCurveFloat* DistanceBiasCurve
    float DistanceBiasWeight,
    UTCATInfluenceComponent* InfluenceComponent
);
