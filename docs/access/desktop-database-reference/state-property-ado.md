---
title: Свойство State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722825"
---
# <a name="state-property-ado"></a><span data-ttu-id="247bc-102">Свойство State (ADO)</span><span class="sxs-lookup"><span data-stu-id="247bc-102">State property (ADO)</span></span>


<span data-ttu-id="247bc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="247bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="247bc-104">Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.</span><span class="sxs-lookup"><span data-stu-id="247bc-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="247bc-105">Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="247bc-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="247bc-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="247bc-106">Return value</span></span>

<span data-ttu-id="247bc-107">Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением.</span><span class="sxs-lookup"><span data-stu-id="247bc-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="247bc-108">Значение по умолчанию — **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="247bc-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="247bc-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="247bc-109">Remarks</span></span>

<span data-ttu-id="247bc-110">Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.</span><span class="sxs-lookup"><span data-stu-id="247bc-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="247bc-111">Свойство **состояние** объекта может содержать комбинацию значений.</span><span class="sxs-lookup"><span data-stu-id="247bc-111">The object's **State** property can have a combination of values.</span></span> <span data-ttu-id="247bc-112">Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="247bc-112">For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="247bc-113">Свойство **State** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="247bc-113">The **State** property is read-only.</span></span>

