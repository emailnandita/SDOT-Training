# SDOT-Training
Coding Practice

clc
clear all
syms x y z
f = input('Enter thye function [P Q R]: ')
P(x,y,z) = f(1); Q(x,y,z) = f(2) ; R(x,y,z) = f(3)
crl = curl(f,[x,y,z])
c1(x,y,z) = crl(1)
c2(x,y,z) = crl(2)
c3(x,y,z) = crl(3)
x = linspace(-4,4,10);
y = x ; z = x;
[X,Y,Z] = meshgrid(x,y,z)
U = P(X,Y,Z)
V = Q(X,Y,Z)
W = R(X,Y,Z)
CR1 = c1(X,Y,Z)
CR2 = c2(X,Y,Z)
CR3 = c3(X,Y,Z)
figure
subplot(1,2,1)
quiver3(X,Y,Z,U,V,W,1)
title('3D view of the vector field')
subplot(1,2,2)
quiver3(X,Y,Z,CR1,CR2,CR3)
title('3D View of curl')


