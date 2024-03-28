# MIST-4610-Group-Project-1

Group Name:
Sp24_47114_Group 1

Group Members:
Isabelle Kiser @isabellekiser

Will Cobb @wjc56122

Bhavik Maniklal @BhavikManiklal

Ty Marcinczyk @TylerMar1

Ryan Schoessling @rschoess3

Jaiden Timmons @jaidentimmons

Client Scenario Overview:
Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club aims to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include many levels of teams, training camps, weekend matches, and special events.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms, a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

Project Problem:
At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, many interconnected elements require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Community FC's commitment to excellence in our local soccer community.

Data Model:
![317542515-b661c931-e2fb-49a2-a013-38d1e4faba8c](https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/cae34841-20cd-431b-b3c2-731788aafd70)
Our data model is based on the structure of a hypothetical professional soccer club. The Member entity represents individual members of the club. A member can be a player, coach, athletic trainer, etc. This is represented by the “role” attribute within Member. A member is further detailed by the entity Membership which is related to Member with a many-to-one relationship. A member may have multiple membership types if they have multiple duties with the club.

Member is also related to Transactions with a one-to-many relationship which shows that a member can make multiple transactions with the club. Our soccer club also sells merchandise. The transaction is related to the Merchandise entity through a many-to-one relationship. This represents that a piece of merchandise can be sold in multiple transactions.

Our soccer club has many different teams ranging from the highest level professional teams to many developmental teams where we have players that we believe will one day be good enough to play on our top team. The Team entity is related to Member with a many-to-many relationship through the associative entity MemberTeam. MemberTeam represents the different team members on each team.

Since we have multiple teams with different skill levels, naturally they play in different leagues. The League entity is related to Team through a one-to-many relationship. This is because a league hold host to many different teams, but a team can only play in one league.

Each team has several different matches they play throughout the season. This is why Team is related to the Matches entity through a many-to-many relationship with the associated entity TeamMatches. TeamMatches represents the individual matches and which team played in the match.

Our players will only get better if they practice their craft. This is why we host multiple training sessions per week. Team is connected to the TrainingSession entity by a one-to-many relationship. This represents how one team has many different training sessions. These training sessions take place in one of our state-of-the-art facilities. The Facility entity is connected to TrainingSession by a one-to-many relationship because a facility can host many different training sessions.

Since our facilities are so nice, we also host matches in these facilities. This is why Facility has a one-to-many relationship with the Matches entity. One facility will host many matches.

Being such a popular soccer club, we have many spectators at every game. The spectators have to buy tickets to gain admission to the matches. This is why there is a one-to-many relationship between Matches and the Ticket entity. One match will have many tickets.

Data Dictionary:

<img width="664" alt="317542791-fa573d2b-8523-4ac4-9abc-d61e64b83a9f" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/e17bbe01-e500-44d4-bc4c-2415421c6f7f">
<img width="655" alt="317542747-9801610b-9b8f-4015-a864-111e297df126" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/abeceb09-5158-4dda-9513-b5de9a8333a8">
<img width="661" alt="56a24bc3-5a8e-43db-8f69-3bf2d102536c" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/ccd856d2-7c51-4727-a357-4cdf03a375b4">
<img width="663" alt="2ac438ec-907c-4c0e-8249-04e122cd660f" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/1edee3d5-09a5-4fcc-aa9f-24a0dbab4936">
<img width="640" alt="691eb359-34ed-4ddf-975f-71f06002a6e7" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/1fadd77d-653c-4795-91bb-99a36fdeaa68">
<img width="652" alt="a227f9e9-d186-4692-beac-f490b27475f1" src="https://github.com/rschoess3/MIST-4610-Group-Project-1/assets/164922893/b09e4d73-e4b8-4ac9-bdc4-0aa4ebeed212">






