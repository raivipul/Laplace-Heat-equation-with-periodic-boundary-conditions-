# Laplace-Heat-equation-with-periodic-boundary-conditions-
#### Discretization Scheme :An explicit finite difference method is used to discretize the governing equation. 
At any interior grid point $(i,j)$ the following equation is valid : $$T_{i,j}^{'} = T_{i,j}^{t} + \frac{ \epsilon}{4}(T_{i+1,j}^{t} + T_{i,j+1}^{t} +T_{i-1,j}^{t} +T_{i,j-1}^{t} -4 T_{i,j}^{t} )$$
At the left boundary  using periodic boundary condition :   $$(i = 0, j = 1 \xrightarrow[]{} N_y -1)   $$ 
Then $T_{0,j}^{t} = T_{N_x - 1,j}^{t}$ 
in equation 2d thermal equation
$$T_{0,j}^{'} = T_{0,j}^{t} + \frac{ \epsilon}{4}(T_{1,j}^{t} + T_{0,j+1}^{t} +T_{N_x - 1,j}^{t} +T_{0,j-1}^{t} -4 T_{0,j}^{t})$$
At the right boundary using periodic boundary condition :
$$(i = N_x - 1, j = 1 \xrightarrow[]{} N_y -1)  $$ 
Then $T_{0,j}^{t} = T_{N_x - 1,j}^{t}$
gives
$$T_{N_x - 1,j}^{'} = T_{N_x - 1,j}^{t} + \frac{ \epsilon}{4}(T_{0,j}^{t} + T_{N_x - 1,j+1}^{t} +T_{N_x - 1,j}^{t} +T_{N_x - 1,j-1}^{t} -4 T_{N_x - 1,j}^{t})$$
Note that $(-1,j)$ and ($N_x,j$) are fictitious points outside the computational domain placed at distance of $\Delta x$ from the left and horizontal boundaries
