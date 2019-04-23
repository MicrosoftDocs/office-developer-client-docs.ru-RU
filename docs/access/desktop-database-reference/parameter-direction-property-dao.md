---
title: Свойство Parameter. Direction (DAO)
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
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="91458-102">Свойство Parameter. Direction (DAO)</span><span class="sxs-lookup"><span data-stu-id="91458-102">Parameter.Direction property (DAO)</span></span>


<span data-ttu-id="91458-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91458-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="91458-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91458-104">Syntax</span></span>

<span data-ttu-id="91458-105">*Expression* . Направлении</span><span class="sxs-lookup"><span data-stu-id="91458-105">*expression* .Direction</span></span>

<span data-ttu-id="91458-106">*Expression (выражение* ) Переменная, представляющая объект **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="91458-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91458-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="91458-107">Remarks</span></span>

<span data-ttu-id="91458-108">Параметр или возвращаемое значение — это значение типа Long, которое может быть равно одной из констант **[параметердиректионенум](parameterdirectionenum-enumeration-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="91458-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="91458-109">Используйте свойство **Direction** , чтобы определить, является ли параметр входным (Output), параметром OUTPUT, или возвращаемым значением из процедуры.</span><span class="sxs-lookup"><span data-stu-id="91458-109">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure.</span></span> <span data-ttu-id="91458-110">Некоторые драйверы ODBC не предоставляют информацию о направлении параметров в инструкцию SELECT или вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="91458-110">Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call.</span></span> <span data-ttu-id="91458-111">В таких случаях необходимо задать направление перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="91458-111">In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="91458-112">Например, следующая процедура возвращает значение из хранимой процедуры с именем "Get\_Employees":</span><span class="sxs-lookup"><span data-stu-id="91458-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="91458-113">{?</span><span class="sxs-lookup"><span data-stu-id="91458-113"></span></span> <span data-ttu-id="91458-114">= Call Get\_Employees}</span><span class="sxs-lookup"><span data-stu-id="91458-114">= call get\_employees}</span></span>

<span data-ttu-id="91458-115">Этот вызов создает один параметр — возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="91458-115">This call produces one parameter — the return value.</span></span> <span data-ttu-id="91458-116">Необходимо задать для этого параметра Направление **дбпарамаутпут** или **дбпарамретурнвалуе** перед выполнением объекта **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="91458-116">You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="91458-117">Необходимо задать все направления параметров, кроме **дбпараминпут** , прежде чем получать доступ к значениям параметров и перед выполнением объекта **QueryDef**, а также задавать их значения.</span><span class="sxs-lookup"><span data-stu-id="91458-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="91458-118">Для возвращаемых значений следует использовать **дбпарамретурнвалуе** , но в тех случаях, когда этот параметр не поддерживается драйвером или сервером, вместо него можно использовать **дбпарамаутпут** .</span><span class="sxs-lookup"><span data-stu-id="91458-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="91458-119">Драйвер Microsoft SQL Server автоматически задает свойство **Direction** для всех параметров процедуры.</span><span class="sxs-lookup"><span data-stu-id="91458-119">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters.</span></span> <span data-ttu-id="91458-120">Не все драйверы ODBC могут определять направление параметра запроса.</span><span class="sxs-lookup"><span data-stu-id="91458-120">Not all ODBC drivers can determine the direction of a query parameter.</span></span> <span data-ttu-id="91458-121">В таких случаях необходимо задать направление перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="91458-121">In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="91458-122">Пример</span><span class="sxs-lookup"><span data-stu-id="91458-122">Example</span></span>

<span data-ttu-id="91458-123">В этом примере используется свойство **Direction** для настройки параметров запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="91458-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

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

