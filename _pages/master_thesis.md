# Master Thesis Topics

---

## 1. Explainable AI via MILP Surrogate Models
*Supervisor: Q. Louveaux, B. Miftari*

Machine learning models such as decision trees, random forests, and shallow neural networks are powerful predictors, but their internal logic often remains opaque. This thesis proposes to bridge interpretability and optimization by constructing Mixed-Integer Linear Programming (MILP) surrogates that are equivalent or ε-faithful to a given trained model. The structural analysis of these surrogates will enable the extraction of insights that are not directly available from the original model, such as decision boundaries and feature interactions expressed as explicit constraints. A key component of the work will consist in identifying and characterizing disagreement regions — areas where the MILP surrogate and the ML model diverge — and leveraging these regions to pinpoint model weaknesses. The ultimate goal is to use this analysis to guide targeted model improvement. The work sits at the intersection of combinatorial optimization and machine learning, and will require both theoretical rigor and practical implementation skills.

---

## 2. Trading and Portfolio Optimization via ML and MILP
*Supervisor: Q. Louveaux, B. Miftari*

Financial markets are characterized by massive volumes of noisy, non-linear data that classical optimization models struggle to handle alone, while machine learning models lack formal optimality guarantees. This thesis proposes to combine both paradigms: ML models will be trained to learn and represent market dynamics, while MILP formulations will be used to derive optimal, explainable trading decisions under realistic constraints such as transaction costs, position limits, and risk measures. The candidate will investigate how to encode learned market representations into tractable optimization problems, and design algorithms to manage and optimize a portfolio of financial assets. Special attention will be given to the interpretability of the resulting strategies, as explainability is of critical importance in regulated financial environments. Both theoretical contributions (model design, complexity analysis) and empirical validation on real or simulated market data are expected.

---

## 3. Multi-Period Energy System Optimization (2030–2050)
*Supervisor: Q. Louveaux, B. Miftari*

Large-scale energy system planning is traditionally addressed by solving a sequence of independent optimization problems, one per target year (2030, 2040, 2050), passing each solution as a fixed input to the next period. While computationally convenient, this rolling sequential approach suffers from a fundamental limitation: it cannot guarantee global optimality over the full planning horizon. Decisions that appear optimal for 2030 may lock the system into suboptimal trajectories for later decades — a phenomenon known as myopic planning bias — which is particularly critical given the largely irreversible nature of energy infrastructure investments. This thesis proposes to overcome this limitation by developing a unified multi-period optimization framework that jointly optimizes the energy system over the entire 2030–2050 horizon within a single model. The work will involve designing appropriate mathematical formulations, handling the computational challenges of large-scale MILP models, and validating the approach on realistic energy planning instances.

---

## 4. FastSchur: Empirical Analysis of a Meta-Solver for Linear Sensitivities
*Supervisor: Q. Louveaux, G. Derval*

Recent theoretical work (Derval, Ernst, Louveaux, Miftari, 2025) introduced efficient algorithms for computing linear sensitivities of linear programs. However, the accompanying implementation is limited to toy problems and has not been developed into a robust, general-purpose solver. This thesis aims to fill that gap by providing a polished implementation of the FastSchur algorithms and conducting a thorough empirical analysis of their behavior on a broad range of problem instances. The candidate will study computational performance, numerical stability, and scalability, comparing the new approach against existing sensitivity analysis methods. The work will require solid programming skills, a good understanding of linear algebra and linear programming, and an interest in the practical aspects of numerical optimization software. The resulting tool is expected to be a concrete contribution to the open-source optimization community.

---

## 5. Measuring the Effective Commercial Speed of Belgian Public Transportation
*Supervisor: Q. Louveaux, G. Derval*

Despite the existence of published statistics on individual train and bus lines, there is no large-scale, end-to-end estimate of the commercial speed of the Belgian public transportation system when combining multiple modes (train, tram, bus). This thesis proposes to produce such an estimate by exploiting open data from SNCB/NMBS, Infrabel, TEC, De Lijn, and STIB, combined with the 2011 Belgian Census commuter matrix. The candidate will model and analyze multi-modal journeys for realistic origin-destination pairs, quantifying travel times and comparing them against alternative modes such as car and bicycle. A particular focus will be placed on transfer times and schedule coordination, which are often the main bottleneck in multi-modal travel. The results will provide a data-driven picture of the adequacy of public transportation for daily commuting in Belgium, and may inform future policy recommendations.

---

## 6. Redefining Train Punctuality: A User-Weighted Analysis of SNCB Delays
*Supervisor: Q. Louveaux, G. Derval*

The SNCB/NMBS officially reports that over 91% of trains run on time, yet many daily users find this figure hard to reconcile with their experience. The discrepancy stems largely from the official definition of lateness, which only counts delays at final destinations and entry/exit points of Brussels, and which does not weight trains by the number of passengers affected. This thesis proposes an alternative, more representative punctuality metric that accounts for delays at all intermediate stops and weights each late train by the number of impacted travellers at each moment of the day. Open data from SNCB/NMBS and Infrabel will be combined with the 2011 Belgian Census commuter matrix to estimate passenger loads per train per time slot. The candidate will design the new KPI, implement the full data pipeline, and produce a comprehensive analysis that compares the new metric to the official one across lines, time periods, and geographic areas.

---

## 7. A Fast and Memory-Efficient Data Structure for Sparse Polynomial Expressions
*Supervisor: Q. Louveaux, G. Derval*

Optimization modelling languages such as Pyomo, GBOML, and JuMP need to store and manipulate large tensors of symbolic expressions. While specialized structures exist for linear and quadratic expressions, no widely available and efficient data structure currently handles general sparse polynomial expressions of moderate degree (up to 16) defined over high-dimensional tensors with potentially millions of indices per dimension. This thesis proposes to design and implement such a data structure in Python, with a focus on memory efficiency, computational performance, and seamless interoperability with NumPy and xarray. Performance-oriented tools such as Cython or Numba will be used to implement compiled kernels and optimized memory access patterns. If time permits, the structure will be extended to support general non-linear expressions represented as operation trees with polynomial leaves. The result is expected to be a reusable, open-source library filling a real gap in the scientific Python ecosystem.

---

## 8. Automatic Course Schedule Generation for Faculties
*Supervisor: Q. Louveaux*

A reorganization of the academic year at the FWB is under discussion, potentially transitioning from two 13-week terms to four 6-week terms plus a project period. This structural change would require all faculties to redesign their course schedules from scratch. This thesis proposes to develop a tool based on Mixed-Integer Programming that can automatically generate course timetables for a faculty, respecting constraints as possibly increasing the options in the curriculum. The tool should be flexible enough to accommodate different organizational criteria that can be customized by the faculty. The candidate will model the scheduling problem mathematically, implement a solver, and validate the approach on real or realistic data from the University of Liège. 

---

## 9. Exam Scheduling and Room Allocation with Mixed-Integer Programming
*Supervisor: Q. Louveaux*

In the context of the potential academic calendar reform described above, all university exams would be concentrated into a single week at the end of each 6-week term, creating a complex joint scheduling and room allocation problem. This thesis investigates the feasibility and performance of Mixed-Integer Programming approaches for solving this problem at university scale. The candidate will formalize the constraints involved — exam duration, student enrolment, room capacity, staff availability, and conflict-free scheduling — and design MILP models to handle them jointly. The computational tractability of the approach will be carefully analyzed, and decomposition or heuristic strategies will be explored if exact methods prove insufficient for large instances. The project offers a concrete application of combinatorial optimization to a problem of direct practical relevance for university administration.

---

## 10. Customizable Navigation System for Cyclists and Hikers
*Supervisor: Q. Louveaux*

Most GPS and navigation systems are designed primarily for car travel, and while some applications offer cycling or hiking routes, they typically provide limited customization. This thesis proposes to build a navigation system tailored to cyclists and hikers, based on OpenStreetMap data and powered by optimization methods. Unlike existing tools, the system will allow users to express personalized preferences — favoring flat terrain, scenic paths, safe road surfaces, or a specific balance between speed and enjoyment — and will compute routes optimized accordingly. The candidate will design the underlying graph model, implement multi-criteria shortest path algorithms, and develop a user interface for preference specification and route visualization. The project combines algorithmic work with practical software development and has the potential to produce a genuinely useful open-source application.

---

## 11. Modular Feature Store for Industrial Data Pipelines
*Supervisor: Q. Louveaux in collaboration with SmartYou *

With the rapid growth of data volumes in industrial environments, there is increasing demand for robust platforms capable of processing, structuring, and storing machine-generated metrics for downstream use by analytics and AI applications. This thesis, carried out in collaboration with SmartYou — a company developing Industry 4.0 solutions — proposes to design and implement a modular feature store fed by the Unified Namespace (UNS) of their Clever Manufacturing Execution System. The work will focus on four key dimensions: adaptability (generic, configurable pipelines deployable across heterogeneous machines), performance (scalable processing under high data throughput), data accessibility (simple and reliable APIs for consuming applications), and observability (monitoring tools for anomaly detection and pipeline supervision). The candidate will gain hands-on experience with real industrial data and constraints, producing a concrete solution that integrates data engineering, software architecture, and applied machine learning concepts acquired during their studies.

---

## 12. Cooperative Multi-Agent AI for a Grid-Based Strategic Game
*Supervisor: Q. Louveaux, A. Tayachi*

Designing AI agents that cooperate effectively in a shared environment is a fundamental challenge in multi-agent systems research. This thesis proposes to design and implement a system of multiple AI agents capable of coordinated strategic behavior in a simplified grid-based game inspired by competitive scenarios such as capture-the-flag. Each agent makes decisions independently, yet the team must develop collective strategies — including role assignment, spatial positioning, and adaptive responses to opponent behavior — in order to maximize a shared objective. The candidate will implement and compare different coordination mechanisms, ranging from rule-based cooperation to learned policies, and evaluate how team performance evolves as cooperation improves over purely independent decision-making. The project offers a hands-on introduction to multi-agent reinforcement learning and game-theoretic reasoning, with clear experimental benchmarks and ample room for creative algorithmic contributions.

---

## 13. Adaptive AI Interview System with Behavioral Analysis
*Supervisor: Q. Louveaux, A. Tayachi*

Job interview preparation is a skill that benefits greatly from realistic, personalized practice, yet existing interview simulators tend to follow rigid, pre-scripted question sequences. This thesis proposes to develop an advanced AI-based interview system that adapts dynamically to the candidate's responses. The system will track performance across multiple turns to assess consistency, clarity, and depth of understanding, adjusting its questioning strategy to probe weaknesses and evaluate key competencies. A multi-agent architecture will be explored, in which specialized agents — such as an HR interviewer, a technical evaluator, and a critical reviewer — collaborate to generate structured, actionable feedback. The candidate will investigate techniques for behavioral profiling and response consistency analysis, and design evaluation protocols to validate the system against human assessors. The project combines natural language processing, multi-agent system design, and human-computer interaction into a practically motivated application.

---

## 14. Algorithmic Improvement of a Shareholding Structure Analysis Tool
*Supervisors: Q. Louveaux, Y. Crama — in collaboration with Zeno-Indices*

Zeno-Indices is a young spin-off of the University of Liège specializing in the analysis of corporate shareholding structures. The company has developed a Python-based software whose core algorithmic engine is grounded in the scientific work of Crama and Leruth (2007) on control and voting power in corporate networks. This thesis, carried out in direct collaboration with the company, proposes to contribute to the improvement and extension of this software along several complementary directions. The candidate will work on accelerating the performance of existing algorithms, designing and implementing alternative algorithmic approaches, and conducting extensive numerical testing covering stability, speed, and robustness across a range of real-world instances. Beyond performance, the project also involves developing new features and improving the overall software architecture. The ideal candidate is passionate about combinatorial algorithm development — particularly in the domains of graph theory and simulation — and is comfortable working autonomously in the dynamic environment of a young fintech startup. This thesis offers a rare opportunity to contribute directly to a commercially deployed product while deepening expertise in both optimization and software engineering.

---

## 15. Predictive Maintenance via Machine Learning in an Industrial Setting
*Supervisors: Q. Louveaux in collaboration with SmartYou collaboration *

As industries transition towards increasingly data-driven environments, predictive maintenance has emerged as one of the most compelling applications of machine learning in the industrial domain. Rather than reacting to equipment failures after the fact, predictive maintenance systems anticipate problems by continuously analysing sensor data — reducing downtime, optimising resource allocation, and extending the lifespan of critical machinery. This thesis, carried out in collaboration with SmartYou and their Clever Manufacturing Execution System (MES), proposes to develop a reliable predictive maintenance model trained on real industrial data collected through the company's Unified Namespace (UNS). Crucially, the project goes well beyond pure model development: a substantial MLOps component is central to the work, covering the full pipeline from data collection and preprocessing to automated model deployment and continuous monitoring. Concretely, the candidate will design training datasets, develop and evaluate machine learning models, implement automated deployment workflows for validated models, and build monitoring systems to track both input data quality and model output drift in production. The result will be a robust, end-to-end AI solution deployable in a real factory environment. This thesis is ideal for a student eager to gain hands-on experience with the full lifecycle of an industrial AI project, from raw data to production system.