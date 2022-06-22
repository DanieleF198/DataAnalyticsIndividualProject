Format of the problem files for the TPP-FSO:
----------------------------------------------------------------------------------------------
NAME : <problem name>
|V| : <number of nodes>
|K| : <number of products>
D : <duration time limit>
NODE_COORD_SECTION
<node id> <x-coordinate> <y-coordinate>
DEMAND_SECTION
<number of products>
<product id> <demand amount>
OFFER_SECTION
node id> <number of products offered by the market> [<product id> <product cost> <product's availability>]...
SERVICE_TIME_SECTION
<node id> <standard service time> <fast service time>
FAST_SERVICE_COST_SECTION
<node id> <fast service cost>
EOF
----------------------------------------------------------------------------------------------
Notice that the node with the label "1" is always the depot, and no offer amount, service time, and service cost are presented for the depot node.
For each pair of nodes, the traveling distance is calculated as c[i,j]=floor(sqrt((x[i]-x[j])^2+(y[i]-y[j])^2)).
Traveling time for each pair of nodes is equal to traveling distance (t[i,j]=c[i,j]).
