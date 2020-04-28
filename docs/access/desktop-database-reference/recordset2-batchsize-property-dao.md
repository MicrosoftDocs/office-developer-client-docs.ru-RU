---
title: Свойство Recordset2. BatchSize (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307471"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="179d5-102">Свойство Recordset2. BatchSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="179d5-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="179d5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="179d5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="179d5-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="179d5-104">Syntax</span></span>

<span data-ttu-id="179d5-105">*Expression* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="179d5-105">*expression* .BatchSize</span></span>

<span data-ttu-id="179d5-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="179d5-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="179d5-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="179d5-107">Remarks</span></span>

<span data-ttu-id="179d5-108">Свойство **BatchSize** определяет размер пакета, используемый при отправке инструкций на сервер при пакетном обновлении.</span><span class="sxs-lookup"><span data-stu-id="179d5-108">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update.</span></span> <span data-ttu-id="179d5-109">Значение свойства определяет количество операторов, отправляемых на сервер, в одном буфере команд.</span><span class="sxs-lookup"><span data-stu-id="179d5-109">The value of the property determines the number of statements sent to the server in one command buffer.</span></span> <span data-ttu-id="179d5-110">По умолчанию 15 операторов отправляются на сервер в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="179d5-110">By default, 15 statements are sent to the server in each batch.</span></span> <span data-ttu-id="179d5-111">Это свойство можно изменить в любое время.</span><span class="sxs-lookup"><span data-stu-id="179d5-111">This property can be changed at any time.</span></span> <span data-ttu-id="179d5-112">Если сервер базы данных не поддерживает пакетную обработку инструкций, для этого свойства можно задать значение 1, в результате чего каждый оператор будет отправлен отдельно.</span><span class="sxs-lookup"><span data-stu-id="179d5-112">If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="179d5-113">Пример</span><span class="sxs-lookup"><span data-stu-id="179d5-113">Example</span></span>

<span data-ttu-id="179d5-114">В этом примере используются свойства **BatchSize** и **UpdateOptions** для управления аспектами обновления пакетов для указанного объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="179d5-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

