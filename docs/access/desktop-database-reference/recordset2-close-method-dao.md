---
title: Метод Recordset2. Close (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307387"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="2ab80-102">Метод Recordset2. Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ab80-102">Recordset2.Close method (DAO)</span></span>


<span data-ttu-id="2ab80-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ab80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ab80-104">Закрывает открытый объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2ab80-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ab80-105">Syntax</span></span>

<span data-ttu-id="2ab80-106">*выражение*.Close</span><span class="sxs-lookup"><span data-stu-id="2ab80-106">*expression* .Close</span></span>

<span data-ttu-id="2ab80-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="2ab80-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab80-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ab80-108">Remarks</span></span>

<span data-ttu-id="2ab80-109">Если на момент использования метода **Close** объект **Recordset** уже закрыт, возникнет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2ab80-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="2ab80-110">Если вы попытаетесь закрыть объект **Connection**, у которого имеются какие-либо открытые объекты **Recordset**, объекты **Recordset** будут закрыты, и все ожидающие операции обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="2ab80-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="2ab80-111">Аналогично, если вы попытаетесь закрыть объект **Workspace**, у которого имеются какие-либо открытые объекты **Connection**, эти объекты **Connection** будут закрыты, что приведет к закрытию их объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2ab80-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="2ab80-112">Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="2ab80-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

