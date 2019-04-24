---
title: Метод Recordset.Close (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f7cbd94bfacc91bfe080d33807ca7989c1dca661
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300555"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="b73fd-102">Метод Recordset.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="b73fd-102">Recordset.Close method (DAO)</span></span>


<span data-ttu-id="b73fd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b73fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b73fd-104">Закрывает открытый объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b73fd-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b73fd-105">Syntax</span></span>

<span data-ttu-id="b73fd-106">*выражение*.Close</span><span class="sxs-lookup"><span data-stu-id="b73fd-106">*expression* .Close</span></span>

<span data-ttu-id="b73fd-107">*выражение* Переменная, которая представляет объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b73fd-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b73fd-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b73fd-108">Remarks</span></span>

<span data-ttu-id="b73fd-109">Если на момент использования метода **Close** объект **Recordset** уже закрыт, возникнет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b73fd-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="b73fd-110">Если вы попытаетесь закрыть объект **Connection**, у которого имеются какие-либо открытые объекты **Recordset**, объекты **Recordset** будут закрыты, и все ожидающие операции обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="b73fd-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="b73fd-111">Аналогично, если вы попытаетесь закрыть объект **Workspace**, у которого имеются какие-либо открытые объекты **Connection**, эти объекты **Connection** будут закрыты, что приведет к закрытию их объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b73fd-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="b73fd-112">Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="b73fd-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

