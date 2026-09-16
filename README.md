# R02-1FA05-ALFORQUE.py
Clean Code Makeover and GitHub Upload
"""
Program Name: Distance Calculator
Description: Calculates the distance between two points (x1, y1) and (x2, y2) 
             using the Euclidean distance formula.
"""

import math

def calculate_distance(x1, y1, x2, y2):
    """Calculates the Euclidean distance between two 2D points."""
    # Apply the distance formula: sqrt((x2 - x1)^2 + (y2 - y1)^2)
    horizontal_difference_squared = (x2 - x1) ** 2
    vertical_difference_squared = (y2 - y1) ** 2
    
    distance = math.sqrt(horizontal_difference_squared + vertical_difference_squared)
    return distance

def main():
    print("=== Distance Calculator ===")
    print("Enter the coordinates for two points to find the distance between them.\n")
    
    try:
        # Get coordinates for the first point
        point1_x = float(input("Enter X coordinate for Point 1: "))
        point1_y = float(input("Enter Y coordinate for Point 1: "))
        
        # Get coordinates for the second point
        point2_x = float(input("Enter X coordinate for Point 2: "))
        point2_y = float(input("Enter Y coordinate for Point 2: "))
        
        # Calculate the result
        total_distance = calculate_distance(point1_x, point1_y, point2_x, point2_y)
        
        # Display the result formatted to 2 decimal places
        print(f"\nThe distance between the two points is: {total_distance:.2f}")
        
    except ValueError:
        print("\nError: Please enter valid numerical values for coordinates.")

if __name__ == "__main__":
    main()
