# Exersize
- Each input from 0 to 10 is poor < bad < okay < good < great < exellent (0, 2, 4, 6, 8, 10)
- With the exception of prices being 0 to 5 cheap < moderate < expensive
- Cheap being 10, moderate being 5, expensive being 0

# Initial Weights
- Food: 0.33
- Service: 0.33
- Price: 0.33

# My formula
result = (food * food_weight + service * service_weight + price * price_weight)

# Good resteraunt
A good resteraunt is one that has a result of >=7

Card 1

    Food: Great
    Service: Poor
    Price: Cheap

    Prediction: dislike (5.94)

    Adjust
    - Food 0.4 (Seems to matter a lot)
    - service 0.3
    - price 0.3

    Customer Opinion: LIKE

Card 2

    Food: Bad
    Service: Great
    Price: Expensive

    Prediction: Dislike (2.4)

    Adjust
    - None needed (Correct)

    Customer Opinion: DISLIKE

Card 3

    Food: Good
    Service: Okay
    Price: Moderate

    Prediction: Dislike 4.7

    Adjust
    - Food: 0.6 (Seems to still matter a lot)
    - Service: 0.2
    - Price 0.2

    Customer Opinion: LIKE

Card 4

    Food: Poor
    Service: Poor
    Price: Cheap

    Prediction: Dislike 2

    Adjust
    - None needed

    Customer Opinion: DISLIKE

Card 5

    Food: Excellent
    Service: Excellent
    Price: Expensive (Seems to not really affect opinion more than the other two)

    Prediction: Like 8

    Adjust
    - None needed

    Customer Opinion: LIKE

Card 6

    Food: Okay
    Service: Bad
    Price: Moderate

    Prediction: Dislike 3.8

    Adjust
    - None needed

    Customer Opinion: DISLIKE

Card 7

    Food: Great
    Service: Okay
    Price: Cheap

    Prediction: Like 7.6

    Customer Opinion: LIKE

Card 8

    Food: Poor
    Service: Excellent
    Price: Expensive

    Prediction: Dislike 2

    Customer Opinion: DISLIKE

Card 9

    Food: Excellent
    Service: Poor
    Price: Moderate

    Prediction: Like 7

    Customer Opinion: LIKE

Card 10

    Food: Okay
    Service: Okay
    Price: Expensive

    Prediction: Dislike 3.2

    Customer Opinion: DISLIKE

# Test

Card 11

    Food: Good
    Service: Excellent
    Price: Cheap

    Prediction: Like (7.6)

    Customer Opinion: LIKE

Card 12

    Food: Bad
    Service: Bad
    Price: Expensive

    Prediction: dislike (1.6)

    Customer Opinion: DISLIKE

Card 13

    Food: Excellent
    Service: Great
    Price: Moderate

    Prediction: Like (8.2)

    Customer Opinion: LIKE

# Final formula

    (food * 0.6 + service * 0.2 + price * 0.2) = result
    if result > 7:
        Like
    else:
        Dislike

# How did your predictions improve?

My predictions improved by more accuratly reflecting the customer's opinion after changing the item that made the final result deviate the most

# How did "weights" (tokens) help you learn?

That a decision can be reached using random numbers given enough adjustments

# What would happen with more layers or inputs?

More considerations could be made to what is good or bad
More layers can result in more thinking and reflecting

# How does this reflect how real AI works?

Real AI uses tokens to drive their behavior. Like if you don't want the AI to do something, punish it by adjusting that token lower. Real AI uses a lot more tokens than this to simulate "neurons"