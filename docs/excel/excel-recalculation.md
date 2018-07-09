---
title: �������� � Excel
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807221"
---
# <a name="excel-recalculation"></a><span data-ttu-id="5818b-104">�������� � Excel</span><span class="sxs-lookup"><span data-stu-id="5818b-104">Excel Recalculation</span></span>

 <span data-ttu-id="5818b-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5818b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5818b-106">������������ ����� �������� �������� � Microsoft Excel ����������� ���������, ��������:</span><span class="sxs-lookup"><span data-stu-id="5818b-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="5818b-107">����� ����� ����� ������ (���� Excel ��������� � ������ ��������������� ���������, ��������� ����� � ���� ������);</span><span class="sxs-lookup"><span data-stu-id="5818b-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="5818b-108">����� ��������� Excel ����������� ��� ����� ��� �� �����;</span><span class="sxs-lookup"><span data-stu-id="5818b-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="5818b-109">����� �������� ��� ������� ������ ��� �������;</span><span class="sxs-lookup"><span data-stu-id="5818b-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="5818b-110">����� ���������� ����� ��� ���������� ��������� **�������� ����� �����������**;</span><span class="sxs-lookup"><span data-stu-id="5818b-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="5818b-111">����� ���������� ��������� �������� �����������;</span><span class="sxs-lookup"><span data-stu-id="5818b-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="5818b-112">������� ������� �� ����������� ����� ��� �������� (� ������ ��������������� ����������);</span><span class="sxs-lookup"><span data-stu-id="5818b-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="5818b-113">����� ����������, �������������� ��� �������� ��������� �����;</span><span class="sxs-lookup"><span data-stu-id="5818b-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="5818b-114">����� �������������� �����;</span><span class="sxs-lookup"><span data-stu-id="5818b-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="5818b-115">����� ��������� ������� ����� ������������ ������ ������;</span><span class="sxs-lookup"><span data-stu-id="5818b-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="5818b-116">����� ������� ��� ����������� ����� (�� ��������).</span><span class="sxs-lookup"><span data-stu-id="5818b-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5818b-p101">� ���� ������ �� �������� �������� ����� ���������������� �������� ������� ��� ������ ���� ������������� � ����������� ���� ����� �������� ��� ��������. ������������ ��������� ������� ��� ������ ���-����, ����� ��� �����������, ������� ��� ����� ��������� ��������� ������������. ����� �������, ����� "������������" ����� �������� "������������ ���� ������� ��� �������, ���������� �������������".</span><span class="sxs-lookup"><span data-stu-id="5818b-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="5818b-120">�����������, "�������" ������ � ������������� ������</span><span class="sxs-lookup"><span data-stu-id="5818b-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="5818b-121">���������� ������ � Excel ����� ������������� ��� ������� �� ���� ������:</span><span class="sxs-lookup"><span data-stu-id="5818b-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="5818b-122">�������� ������ ������������</span><span class="sxs-lookup"><span data-stu-id="5818b-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="5818b-123">�������� ������� ����������</span><span class="sxs-lookup"><span data-stu-id="5818b-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="5818b-124">�������� �����</span><span class="sxs-lookup"><span data-stu-id="5818b-124">Recalculation of cells</span></span>
    
<span data-ttu-id="5818b-p102">������ ������������ �������� Excel, ����� ������ ������� �� ������ ����� ���, ����������, ����� ������ �������� ������������ ��� ������. �� ����� ������ Excel ���������� ������� ����������. � ��� ������������� ��� ������, ������� �������� �������, � ��� �������, � ������� �� ���������� ���������. �� ����� ��������� Excel �������� ��� �������, ���� �������������� �������, ������� ������� �� ��� �� ����������� ������. � ���� ������ ����������� ������ � ��������� �� ��� ������ ������������ ���� �� �������. �� ���� ������� ����� ���������� � ������ ���������� ������ ����� ����������� �� ������, ������� ���� ������ ��� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="5818b-p103">��� ����������� ��������� �����, �������� ��� ����� ����� �������, Excel ������ ������� ������ ������������ � ������� ����������. ��� ����� ����� ������ ��� ����� ������ Excel �������� ��� ������, ������� ������� �� ����� ������, ��� ��������� ���������. ���������� ����� ������� ������ ����������  *"��������"*  . ��� ������ � ��������� ��������� ������ ���������� ��� "�������", ������� ���� ������ B1 ������� �� ������ A1, � ������ C1 � �� B1, �� ��� ��������� ������ A1 ������ B1 � C1 ���������� ��� "�������".</span><span class="sxs-lookup"><span data-stu-id="5818b-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="5818b-p104">���� ������ �������, ����� ��� ��������, �� ����, �� Excel ������������ ����������� ������ � ������������� ������������. ��� �������, ��� �������� � ������, ������� ������������ ������ ���������, � Excel ������������� �������� ����������� � ������������� ��������, ������� ������� ������������ ����� �������� ����������� �����������. � ��������� ������� ��� ������� ��������� ���������. � �������, ��� ����� ��������� ����������� ����������, ��� ��������� ������ ��� ��������� �������� �������� ��������� ����������. Excel ������������ ���������� ������������ ������������ � ������� ����������� ���� ���������� ����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="5818b-p105">������� ������ ��� "�������" ��� ��������� ���������, Excel �������� ��������� ���������� ������ "�������" ������ � �������, ������������ �������� ����������. � ����������� ���� ������� ��� ��������, ��� ������� ����������� ������ B1, � ����� � C1. �������� ���������� ����� ����� ����, ��� Excel �������� �������� ������ ��� "�������", ���� ������ �������������� ����� ���������. � ��������� ������ ��� ���������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="5818b-p106">������� � Microsoft Excel 2002, ������ **Range** � Microsoft Visual Basic ��� ���������� (VBA) ������������ ����� **Range.Dirty**, ������� �������� ������ ��� ��������� ��������. ����� �� ������������ ��������� � ������� **Range.Calculate** (��. ��������� ������), �� �������� �������������� �������� ����� � ������������ ���������. ��� ������� ��� ���������� ������������� ���������� � �������, ��� ���������� ������ ����� ����������, �� ��������� ������� ����������� �����, �� ����������� � ������� �������. ������ ���������� ���������� ���������� ����� API C.</span><span class="sxs-lookup"><span data-stu-id="5818b-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="5818b-p107">� Excel 2002 � ����� ������ ������� Excel ��������� ������� ���������� ��� ������� ����� � ������ �������� �����. ��� ��������� ��������� ��������� ������ ����� ������� � ��������� ������������ ��� ����������� ������������ ���������. � ���������, � Excel 2000 ���������� ������� � �������� ����������� ����� ������� � ����������� ������ ����� � ���������� �������, ����� �����, ��������� �� ������ ������, ��������� �� �������� �� �������, �� ������� ��� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="5818b-p108">� Excel�2007 ������ ���� �������� ��� ��������� ��������� � ��������� �������, ����� ������� ������� ���������� �� �������� ���� �� ����� � �� ����� ���� ��������� ������������. �� ������ ��������� Excel ��� ������������� ���������� ������� �� ���������� � ����� ����������� ��� ������ ������ �� ����������������� ��� ������������ ����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="5818b-152">����������� ���������������� �������</span><span class="sxs-lookup"><span data-stu-id="5818b-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="5818b-p109">����� ���������� ������������ ����������� ���������������� �������, ��� ��������� ��������� ������� �������, ��������� ���������������� ������� � ���������� ��������� ��������� ������. ����� ���������� ��������� ������ �����, Excel ���� ���������� ����������� �������, ���� ��� ��� �����������. �� ���� ���� ��� ������ ����������� ������� �������� � �����������, Excel ��������� �������, � ����� ��������� ����� �������� ����������, ����� ����������� ������, ������� ���������� ������ �� ������� �� ����������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="5818b-156">���������� � ���������� �������</span><span class="sxs-lookup"><span data-stu-id="5818b-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="5818b-p110">Excel ������������ ���������� �������, �� ���� �������, �������� ������� � ������ ������� ����� ����������, ���� ���� �� ���� �� ���������� (���� ��� �����������) �� ���������. Excel �������� ��������� ������, ������� �������� ���������� �������, ������ �� ����� ���������� ��������� ��� ������ ���������. �� ���� ������� ���������� ������������� ���������� ������� ����� ��������� ��������. ����������� �� ��������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="5818b-161">����������� �������� ��������� ������� Excel:</span><span class="sxs-lookup"><span data-stu-id="5818b-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="5818b-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="5818b-162">**NOW**</span></span>
    
- <span data-ttu-id="5818b-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="5818b-163">**TODAY**</span></span>
    
- <span data-ttu-id="5818b-164">**СЛУЧМЕЖДУ()**</span><span class="sxs-lookup"><span data-stu-id="5818b-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="5818b-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="5818b-165">**OFFSET**</span></span>
    
- <span data-ttu-id="5818b-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="5818b-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="5818b-167">**INFO** (� ����������� �� ����������)</span><span class="sxs-lookup"><span data-stu-id="5818b-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="5818b-168">**CELL** (� ����������� �� ����������)</span><span class="sxs-lookup"><span data-stu-id="5818b-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="5818b-169">**СУММЕСЛИ** (в зависимости от его аргументов)</span><span class="sxs-lookup"><span data-stu-id="5818b-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="5818b-p111">���������� API VBA � C ������������ ������� �������� Excel, ��� ���������������� ������� ������� ������������ ��� ����������. � VBA ���������������� ������� ����������� ���������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="5818b-p112">�� ��������� Excel ������������, ��� ���������������� ������� VBA �� �������� �����������. Excel ������, ��� ���������������� ������� �������� ����������, ������ ��� �� ������ ������. ���������� ���������������� ������� ����� ������� ����������, ��� � ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="5818b-p113">� ������� API C ����� ���������������� ������� XLL ��� ���������� �� �� ������� ������. �� ����� ��������� �������� � ��������� ���������� ��������� ������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="5818b-p114">�� ��������� Excel ������������ ���������������� ������� XLL, ������� ��������� ��������� � �������� ���������� � ��������� ��� ����������� ����� ��������, ��� ����������. �� ������ ��������� ��� ��������� �� ��������� � ������� ������� **xlfVolatile** ��� ������ ������ ���������������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="5818b-179">������ ����������, �������, ���������� �������� � ������� ������</span><span class="sxs-lookup"><span data-stu-id="5818b-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="5818b-180">� Excel ���� ��� ������ ����������:</span><span class="sxs-lookup"><span data-stu-id="5818b-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="5818b-181">��������������</span><span class="sxs-lookup"><span data-stu-id="5818b-181">Automatic</span></span>
    
- <span data-ttu-id="5818b-182">��������������, ����� ������</span><span class="sxs-lookup"><span data-stu-id="5818b-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="5818b-183">������</span><span class="sxs-lookup"><span data-stu-id="5818b-183">Manual</span></span>
    
<span data-ttu-id="5818b-p115">� �������������� ������ ���������� �������� ���������� ������ ����� ������� ����� ������ � ����� ������������ �������, ����� ��� ������� � ���������� �������. � ����� ������� ������ �������� ����� �������� ��� ����� �������, ��� ������������� ���������� ������������ ��� �������, ����� �������� ���������� ������ ��� �������������. ��� ����� Excel ������������ ������ �����. ������������ ����� ������� ����� � ������� ���� Excel ��� ����������� �������� � ������� API VBA, COM ��� C.</span><span class="sxs-lookup"><span data-stu-id="5818b-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="5818b-p116">������� ������ � ��� ����������� ��������� �� �����. ������� ������������ ����������� ���������� ���������� �� �����. ��� ������� �� ������ ��� ���� ���������� ��������� ������ � ������ ����������. ����� ������������ ����� ������� ������� ����������� ��� ������ �������� ������ ��� ����� ��������� ������. ������� ��������� � ������� **������� ������ ������**. ����� ��������� ������� Excel �� ������ ���������� ����� � ���������� � �������� ���������� �������� � �������. ��� ��� ����� ������������ ���� ��� ��� �����, ������� ������ ����� ���� ����������� ��� ����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="5818b-195">�������� ������ ������ �������������� ������� ��-�������:</span><span class="sxs-lookup"><span data-stu-id="5818b-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="5818b-196">�������� �������������� ���������� � ������� �� �������� ��������� ����, ������� �������� ������� ������ ����� �������� ������ �������, ��� �������� ��������� ��������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="5818b-p117">����������� ������ �����������. ���� ����������, ������������ ��� ��������� ����������, ������� �� ������ ��� ���������� �������� �� ������� ������, �� Excel �� ���������� ������ ����������� �����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="5818b-p118">��������, ��� Excel ��-������� ������������ �������� ������ ������, � ���������� ������� ������, ��������� �� ������� ��� ������� ����������, ����� �������� ����� �������, Excel ��������� ��������� �������������� ���������� ������ ������. ��� ����� �������� ����� ���������� "��������������, ����� ������". � ���� ������ ������������ ����� ������������� ������, ����� ������� F9 ��� �������� ������������� ����������� ��������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="5818b-p119">Excel ������������� ������, � ������� ������� ����� �������� ����� ��������� � ��������� ��. ��� ������ ���������� �� ������ � ������, ����� ���������� ����������� ����� ������� ����������. ����������� API C � ���� ��������� �������� �����������, ��������� � Excel ������ 5, ������� �� ������������� ������ ����������, ��� ��� ������������� VBA � ����� ������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="5818b-205">��� ������ ���� ����� ������������, ����� Excel ��������� � ������ ������ ����������, � ��������� ��������� ��������� �����, ����� � ���������, ��������� ������������� ��� �������� ����� � ���� ��������� ������������� ������ ������������ � ������� ����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="5818b-206">���������� ����������</span><span class="sxs-lookup"><span data-stu-id="5818b-206">Range Calculation</span></span>

<span data-ttu-id="5818b-207">�������: ���</span><span class="sxs-lookup"><span data-stu-id="5818b-207">Keystroke: None</span></span>
  
<span data-ttu-id="5818b-208">VBA: **Range.Calculate** (�������� � Excel 2000, ������� � Excel�2007) � **Range.CalculateRowMajorOrder** (�������� � Excel�2007)</span><span class="sxs-lookup"><span data-stu-id="5818b-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="5818b-209">API C: �� ��������������</span><span class="sxs-lookup"><span data-stu-id="5818b-209">C API: Not supported</span></span>
  
- <span data-ttu-id="5818b-210">**������ �����**</span><span class="sxs-lookup"><span data-stu-id="5818b-210">**Manual mode**</span></span>
    
    <span data-ttu-id="5818b-p120">������������� ������ ������ � ������������ ��������� ���������� �� ����, "�������" �� ���. ��������� ������ **Range.Calculate** ���������� � Excel�2007. ��� �� �����, ������ ��������� ��-�������� �������������� � **Range.CalculateRowMajorOrder** method.</span><span class="sxs-lookup"><span data-stu-id="5818b-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="5818b-213">**����� "��������������" ��� "��������������, ����� ������"**</span><span class="sxs-lookup"><span data-stu-id="5818b-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="5818b-214">������������� �����, �� �� ��������� �������������� �������� ��������� ��� �����-���� ����� � ���.</span><span class="sxs-lookup"><span data-stu-id="5818b-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="5818b-215">�������� ���������� ������</span><span class="sxs-lookup"><span data-stu-id="5818b-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="5818b-216">�������: SHIFT+F9</span><span class="sxs-lookup"><span data-stu-id="5818b-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="5818b-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="5818b-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="5818b-218">API C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="5818b-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="5818b-219">**��� ������**</span><span class="sxs-lookup"><span data-stu-id="5818b-219">**All modes**</span></span>
    
    <span data-ttu-id="5818b-220">������������� ������, ���������� ��� ����������, ������ �� �������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="5818b-221">���������� ��������� ������</span><span class="sxs-lookup"><span data-stu-id="5818b-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="5818b-222">�������: ���</span><span class="sxs-lookup"><span data-stu-id="5818b-222">Keystroke: None</span></span>
  
<span data-ttu-id="5818b-223">VBA: **Worksheets(** ������ **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="5818b-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="5818b-224">API C: �� ��������������</span><span class="sxs-lookup"><span data-stu-id="5818b-224">C API: Not supported</span></span>
  
- <span data-ttu-id="5818b-225">**��� ������**</span><span class="sxs-lookup"><span data-stu-id="5818b-225">**All modes**</span></span>
    
    <span data-ttu-id="5818b-p121">������������� "�������" ������ � �� ����������� ������ �� ��������� �����. ������ � ��� ��� ����� ��� ������ ��� ����� ������� � ��������������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="5818b-p122">Excel 2000 � ����� ������� ������ ������������� �������� ����� **EnableCalculation** � ������� **Boolean**. ���� ������ ��� ���� �������� **True** ������ **False**, ��� ������ �� ��������� ����� ����� �������� ��� "�������". � �������������� ������� ��� ����� �������� �������� ���� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="5818b-231">� ������ ������ ��������� ��� �������� �������� ������ ��������� �����.</span><span class="sxs-lookup"><span data-stu-id="5818b-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="5818b-232">��������� �������� � �������������� �������� ������ �����</span><span class="sxs-lookup"><span data-stu-id="5818b-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="5818b-233">�������: CTRL+ALT+SHIFT+F9 (��������� � Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="5818b-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="5818b-234">VBA: **Workbooks(** ������ **).ForceFullCalculation** (��������� � Excel�2007)</span><span class="sxs-lookup"><span data-stu-id="5818b-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="5818b-235">API C: �� ��������������</span><span class="sxs-lookup"><span data-stu-id="5818b-235">C API: Not supported</span></span>
  
- <span data-ttu-id="5818b-236">**��� ������**</span><span class="sxs-lookup"><span data-stu-id="5818b-236">**All modes**</span></span>
    
    <span data-ttu-id="5818b-237">��������� Excel ������ ������� ������ ������������ � ������� ���������� ��� ������������ ����� � �������� �������� ���� �����, ���������� �������.</span><span class="sxs-lookup"><span data-stu-id="5818b-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="5818b-238">��� �������� �����</span><span class="sxs-lookup"><span data-stu-id="5818b-238">All Open Workbooks</span></span>

<span data-ttu-id="5818b-239">�������: F9</span><span class="sxs-lookup"><span data-stu-id="5818b-239">Keystroke: F9</span></span>
  
<span data-ttu-id="5818b-240">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="5818b-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="5818b-241">API C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="5818b-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="5818b-242">**��� ������**</span><span class="sxs-lookup"><span data-stu-id="5818b-242">**All modes**</span></span>
    
    <span data-ttu-id="5818b-p123">������������� ��� ������, ������� Excel ������� ��� "�������", �� ���� ��������� �� ���������� ��� ���������� ������, � ������, ���������� ���������� ��� "�������". ���� ������ ����� ���������� "��������������, ����� ������", ���� ����� ��������� �������, ������� ������� ����������, � ����� ��� ���������� ������� � �� �����������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="5818b-245">��������� �������� � �������������� ���������� ������ ���� �������� ����</span><span class="sxs-lookup"><span data-stu-id="5818b-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="5818b-246">�������: CTRL+ALT+F9</span><span class="sxs-lookup"><span data-stu-id="5818b-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="5818b-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="5818b-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="5818b-248">API C: �� ��������������</span><span class="sxs-lookup"><span data-stu-id="5818b-248">C API: Not supported</span></span>
  
- <span data-ttu-id="5818b-249">**��� ������**</span><span class="sxs-lookup"><span data-stu-id="5818b-249">**All modes**</span></span>
    
    <span data-ttu-id="5818b-p124">������������� ��� ������ �� ���� �������� ������. ���� ������ ����� ���������� "��������������, ����� ������", ����������� �������������� �������� ������.</span><span class="sxs-lookup"><span data-stu-id="5818b-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5818b-252">��. �����</span><span class="sxs-lookup"><span data-stu-id="5818b-252">See also</span></span>



[<span data-ttu-id="5818b-253">�������������� �������� � Excel</span><span class="sxs-lookup"><span data-stu-id="5818b-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="5818b-254">���� ������, ������������ � Excel</span><span class="sxs-lookup"><span data-stu-id="5818b-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="5818b-255">���������� ������� � Excel</span><span class="sxs-lookup"><span data-stu-id="5818b-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="5818b-256">�������� ���������������� � Excel</span><span class="sxs-lookup"><span data-stu-id="5818b-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

