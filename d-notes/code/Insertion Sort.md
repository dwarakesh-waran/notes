Topic: [[My Learning]]

To understand Insertion Sort better, think of arranging cards while you are playing rummy or other card games.

Steps:
1. You need to know the data of the current card (lets start from the leftmost card)
	1. Data of the current card = card[current]
2. After knowing the data of the current card (lets say 10 Diamond), you need to know the position of the previous card.
	1. Position of the previous card = current - 1 
3. Then you need to compare the data of the current card and the data of the previous card.
	1. while(card[previous] < card[current])
4. If the current card is greater than the previous one, then move the previous card to its next position.
	1. card[previous +1] (next position of the previous card) = card[previous]
5. After doing this, compare the current card to its previous previous card. For doing this, we are already using while loop and all we need to go to the previous previous card is by using decrement operator.
	1. previous--
6. If you find a previous card which is greater than the current card, then **come out of the comparison loop** and assign the current card to the right side of the previous card's position.
	1. card[previous + 1] (right side of the previous card) = card[current]