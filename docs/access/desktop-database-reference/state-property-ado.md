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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308535"
---
# <a name="state-property-ado"></a><span data-ttu-id="20dd0-102">Свойство State (ADO)</span><span class="sxs-lookup"><span data-stu-id="20dd0-102">State property (ADO)</span></span>


<span data-ttu-id="20dd0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20dd0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20dd0-104">Указывает на все применимые объекты, независимо от того, является ли состояние объекта открытым или закрытым.</span><span class="sxs-lookup"><span data-stu-id="20dd0-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="20dd0-105">Указывает для всех применимых объектов, которые выполняют асинхронный метод, независимо от того, подключается ли, выполняется или выполняется текущий объект.</span><span class="sxs-lookup"><span data-stu-id="20dd0-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="20dd0-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20dd0-106">Return value</span></span>

<span data-ttu-id="20dd0-107">Возвращает **длинное значение,** которое может быть [значением ObjectStateEnum.](objectstateenum.md)</span><span class="sxs-lookup"><span data-stu-id="20dd0-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="20dd0-108">Значение по умолчанию **— adStateClosed.**</span><span class="sxs-lookup"><span data-stu-id="20dd0-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20dd0-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="20dd0-109">Remarks</span></span>

<span data-ttu-id="20dd0-110">Свойство State **можно** использовать для определения текущего состояния заданного объекта в любое время.</span><span class="sxs-lookup"><span data-stu-id="20dd0-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="20dd0-111">Свойство **State** объекта может иметь сочетание значений.</span><span class="sxs-lookup"><span data-stu-id="20dd0-111">The object's **State** property can have a combination of values.</span></span> <span data-ttu-id="20dd0-112">Например, если выполняется выписка, это свойство будет иметь комбинированные значения **adStateOpen** и **adStateExecuting.**</span><span class="sxs-lookup"><span data-stu-id="20dd0-112">For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="20dd0-113">Свойство **State** имеет только чтение.</span><span class="sxs-lookup"><span data-stu-id="20dd0-113">The **State** property is read-only.</span></span>

