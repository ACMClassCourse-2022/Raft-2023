# Raft-2023

**注意：** 根据 MIT 课程要求，你的 Raft 代码仓库应为 **私有（PRIVATE）** 类型。

## Reference

[MIT 6.5840 Lab 2](https://pdos.csail.mit.edu/6.824/labs/lab-raft.html)

[MIT 6.5840 Lab 3](https://pdos.csail.mit.edu/6.824/labs/lab-kvraft.html)

## Introduction

Raft is a consensus algorithm for managing a replicated log. It allow a collection of machines to work as a coherent group that can survive all all non-Byzantine conditions, including network delays, partitions, and packet loss, duplication, and reordering. According to the Raft paper, it is more understandable than Paxos.

## Goal

- Learn Golang
- Understand and implement the Raft algorithm
- Build a key/value service on top of Raft (ACM Class)
- Add log compaction for your Raft (bonus)

## Tutorial

See [Tutorial.md](doc/Tutorial.md) in `doc/`.

## Grading

<table border="1" cellpadding="1" cellspacing="1">
	<thead>
		<tr>
			<th scope="col" style="text-align:center">Part</th>
			<th scope="col" style="text-align:center">工科</th>
			<th scope="col" style="text-align:center">ACM Class</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align:center">Lab 2A</td>
			<td style="text-align:center">30%</td>
			<td style="text-align:center">15%</td>
		</tr>
		<tr>
			<td style="text-align:center">Lab 2B</td>
			<td style="text-align:center">50%</td>
			<td style="text-align:center">25%</td>
		</tr>
		<tr>
			<td style="text-align:center">Lab 2C</td>
			<td style="text-align:center">extra 10%</td>
			<td style="text-align:center">25%</td>
		</tr>
		<tr>
			<td style="text-align:center">Lab 2D</td>
			<td colspan="1" rowspan="3" style="text-align:center">/</td>
			<td style="text-align:center">extra 5%</td>
		</tr>
		<tr>
			<td style="text-align:center">Lab 3A</td>
			<td style="text-align:center">15%</td>
		</tr>
		<tr>
			<td style="text-align:center">Lab 3B</td>
			<td style="text-align:center">extra 5%</td>
		</tr>
		<tr>
			<td style="text-align:center">Code Review</td>
			<td colspan="2" rowspan="1" style="text-align:center">20%</td>
		</tr>
	</tbody>
</table>

For each lab, we will run the test for  $400$ times. Let $S$ be the total score of a lab and $t$ be the times you pass. 

- For a required lab,  your score of this lab will be 
  $$\left\lceil\frac{\max\\{t-200,0\\}}{2}\right\rceil\times 0.01\times S.$$

- For a bonus lab, your score of this lab will be

  $$(\max\\{t-380,0\\})^2\times 0.0025\times S.$$

## Schedule

<table border="1" cellpadding="1" cellspacing="1">
	<thead>
		<tr>
			<th scope="col" style="text-align:center">Week</th>
			<th scope="col" style="text-align:center">Day</th>
			<th scope="col" style="text-align:center">工科</th>
			<th scope="col" style="text-align:center">ACM Class</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td colspan="1" rowspan="7" style="text-align:center">3</td>
			<td style="text-align:center">7/3</td>
			<td colspan="2" rowspan="3">
			<div>1. Learn Golang</div>
			<div>2. Read extended Raft paper</div>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">7/4</td>
		</tr>
		<tr>
			<td style="text-align:center">7/5</td>
		</tr>
		<tr>
			<td style="text-align:center">7/6</td>
			<td colspan="2" rowspan="2">3. Try to pass Lab 2A</td>
		</tr>
		<tr>
			<td style="text-align:center">7/7</td>
		</tr>
		<tr>
			<td style="text-align:center">7/8</td>
			<td colspan="2" rowspan="2" style="text-align:center">Break</td>
		</tr>
		<tr>
			<td style="text-align:center">7/9</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="7" style="text-align:center">4</td>
			<td style="text-align:center">7/10</td>
			<td colspan="1" rowspan="4">
			<div>1. Pass Lab 2A (cont.)</div>
			<div>2. Pass Lab 2B</div>
			<div>3. Try Lab 2C (bonus)</div>
			</td>
			<td colspan="1" rowspan="5">
			<div>1. Pass Lab 2A (cont.)</div>
			<div>2. Pass Lab 2B</div>
			<div>3. Try to pass Lab 2C</div>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">7/11</td>
		</tr>
		<tr>
			<td style="text-align:center">7/12</td>
		</tr>
		<tr>
			<td style="text-align:center">7/13</td>
		</tr>
		<tr>
			<td style="text-align:center">7/14</td>
			<td style="text-align:center">Code Review</td>
		</tr>
		<tr>
			<td style="text-align:center">7/15</td>
			<td colspan="1" rowspan="14" style="text-align:center">Summer Vacation</td>
			<td colspan="1" rowspan="2" style="text-align:center">Break</td>
		</tr>
		<tr>
			<td style="text-align:center">7/16</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="7" style="text-align:center">5</td>
			<td style="text-align:center">7/17</td>
			<td colspan="1" rowspan="5">
			<div>1. Pass Lab 2C (cont.)</div>
			<div>2. Learn Linearizability</div>
			<div>3. Try to pass Lab 3A</div>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">7/18</td>
		</tr>
		<tr>
			<td style="text-align:center">7/19</td>
		</tr>
		<tr>
			<td style="text-align:center">7/20</td>
		</tr>
		<tr>
			<td style="text-align:center">7/21</td>
		</tr>
		<tr>
			<td style="text-align:center">7/22</td>
			<td colspan="1" rowspan="2" style="text-align:center">Break</td>
		</tr>
		<tr>
			<td style="text-align:center">7/23</td>
		</tr>
		<tr>
			<td colspan="1" rowspan="5" style="text-align:center">6</td>
			<td style="text-align:center">7/24</td>
			<td colspan="1" rowspan="4">
			<div>1. Pass Lab 3A (cont.)</div>
			<div>2. Try Lab 2D &amp; 3B (bonus)</div>
			</td>
		</tr>
		<tr>
			<td style="text-align:center">7/25</td>
		</tr>
		<tr>
			<td style="text-align:center">7/26</td>
		</tr>
		<tr>
			<td style="text-align:center">7/27</td>
		</tr>
		<tr>
			<td style="text-align:center">7/28</td>
			<td style="text-align:center">Code Review</td>
		</tr>
	</tbody>
</table>
