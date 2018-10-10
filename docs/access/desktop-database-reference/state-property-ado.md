---
title: State Property (ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483030"
---
# <a name="state-property-ado"></a><span data-ttu-id="eb1a8-102">State Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="eb1a8-102">State Property (ADO)</span></span>


<span data-ttu-id="eb1a8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb1a8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb1a8-104">Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="eb1a8-105">Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb1a8-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb1a8-106">Return Value</span></span>

<span data-ttu-id="eb1a8-107">Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="eb1a8-108">Значение по умолчанию — **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1a8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb1a8-109">Remarks</span></span>

<span data-ttu-id="eb1a8-110">Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="eb1a8-111">Свойство **состояние** объекта может содержать комбинацию значений.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-111">The object's **State** property can have a combination of values.</span></span> <span data-ttu-id="eb1a8-112">Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-112">For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="eb1a8-113">Свойство **State** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eb1a8-113">The **State** property is read-only.</span></span>

