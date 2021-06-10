---
title: Свойство Parameter.Direction (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3260fd3f01e8ca22d5be4f8d14f6376c31e2735a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288093"
---
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="45ee6-102">Свойство Parameter.Direction (DAO)</span><span class="sxs-lookup"><span data-stu-id="45ee6-102">Parameter.Direction property (DAO)</span></span>


<span data-ttu-id="45ee6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45ee6-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="45ee6-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45ee6-104">Syntax</span></span>

<span data-ttu-id="45ee6-105">*выражения* . Направление</span><span class="sxs-lookup"><span data-stu-id="45ee6-105">*expression* .Direction</span></span>

<span data-ttu-id="45ee6-106">*выражение* Переменная, представляюная **объект Параметр.**</span><span class="sxs-lookup"><span data-stu-id="45ee6-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ee6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="45ee6-107">Remarks</span></span>

<span data-ttu-id="45ee6-108">Значение параметра или значения возврата — long, которое можно задать одному из констант **[ParameterDirectionEnum.](parameterdirectionenum-enumeration-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="45ee6-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="45ee6-109">Используйте свойство **Direction,** чтобы определить, является ли этот параметр параметром ввода, выходным параметром, как, так и возвратным значением процедуры.</span><span class="sxs-lookup"><span data-stu-id="45ee6-109">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure.</span></span> <span data-ttu-id="45ee6-110">Некоторые драйверы ODBC не предоставляют сведения о направлении параметров в инструкцию SELECT или процедурный вызов.</span><span class="sxs-lookup"><span data-stu-id="45ee6-110">Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call.</span></span> <span data-ttu-id="45ee6-111">В этих случаях необходимо запросить направление перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="45ee6-111">In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="45ee6-112">Например, следующая процедура возвращает значение из сохраненной процедуры с именем "получить \_ сотрудников":</span><span class="sxs-lookup"><span data-stu-id="45ee6-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="45ee6-113">{?</span><span class="sxs-lookup"><span data-stu-id="45ee6-113">{?</span></span> <span data-ttu-id="45ee6-114">= вызов получить \_ сотрудников}</span><span class="sxs-lookup"><span data-stu-id="45ee6-114">= call get\_employees}</span></span>

<span data-ttu-id="45ee6-115">При этом вызове создается один параметр — возвращаемая величина.</span><span class="sxs-lookup"><span data-stu-id="45ee6-115">This call produces one parameter — the return value.</span></span> <span data-ttu-id="45ee6-116">Перед выполнением **[QueryDef](querydef-object-dao.md)** необходимо задать направление этого параметра **dbParamOutput** или **dbParamReturnValue.**</span><span class="sxs-lookup"><span data-stu-id="45ee6-116">You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="45ee6-117">Необходимо задать все направления параметров, за исключением **dbParamInput,** перед доступом или настройкой значений параметров и перед выполнением **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="45ee6-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="45ee6-118">Для возвращаемого значения следует использовать **dbParamReturnValue,** но в случаях, когда этот параметр не поддерживается драйвером или сервером, вместо этого можно использовать **dbParamOutput.**</span><span class="sxs-lookup"><span data-stu-id="45ee6-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="45ee6-119">Драйвер Microsoft SQL Server автоматически задает свойство **Direction** для всех параметров процедуры.</span><span class="sxs-lookup"><span data-stu-id="45ee6-119">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters.</span></span> <span data-ttu-id="45ee6-120">Не все драйверы ODBC могут определять направление параметра запроса.</span><span class="sxs-lookup"><span data-stu-id="45ee6-120">Not all ODBC drivers can determine the direction of a query parameter.</span></span> <span data-ttu-id="45ee6-121">В этих случаях необходимо запросить направление перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="45ee6-121">In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="45ee6-122">Пример</span><span class="sxs-lookup"><span data-stu-id="45ee6-122">Example</span></span>

<span data-ttu-id="45ee6-123">В этом примере **свойство Direction** настраивает параметры запроса на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="45ee6-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

