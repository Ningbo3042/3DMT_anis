# 3DMT_anis
# 3DMT_ani
1. This code is an edge-based and nodal FEM modeling code for solving the 3D MT problem in anisotropic media using vector-scalar potentials.
2. The program is written in language MATLAB.
3. "3Dansmodel.ws" is the model data file
    % The first line is the comment line
    % The second line contains four parameters, which are the number of edges in x,y and z direction in turn, 
         and the fourth parameter is the number of air layers
    % The third line to the seventh line are the lengths of edges along X, Y and Z directions, respectively
    % The sixth line contains three parameters, including the coordinates of measuring points along X and Y directions and the number of frequency points
    % The seventh and eighth lines are the coordinates of measuring points, respectively
    % The ninth line are the frequencies of calculation
    % The tenth line is the comment line of model
    % The following data are resistivity data and Euler angle of the element, respectively
4. Running operation of code
   It can be run only by giving the model parameter file, and Multiple example model files "3Dansmodel.ws" are given here.
   The resistivity of this example is 100/10/100 Ω.m, and the Euler angle is 30°/0°/0°, 60/0°/0°, 0°/30°/0°, and 0°/60°/0°,respectively . The dimensions are shown in figure 4 of the manuscript.
   The forward results of two polarization modes can be obtained by running the main program file "main.m". 
   In addition, The iterative solver needs to be selected, where 'Q' represents the QMR iterative solver and 'B' represents the BICGSTAB iterative solver
where,
   readmodel_data.m and read_model.m are subroutines for reading model data and calculating model data, respectively;
   get_matrix_index.m is the index code of the calculation unit and edge;
   get_matrix.m is used to calculate the stiffness sparse matrix of the model;
   get_boundary.m the electric field for calculating the 1D analytical solution;
   get_XY.m and get_YX.m are calculate the EH fields of two modes (xy mode and yx mode), respectively.
