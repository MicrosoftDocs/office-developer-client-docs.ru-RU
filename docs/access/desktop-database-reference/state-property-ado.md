---
title: Свойство state (ADO)
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
# <a name="state-property-ado"></a><span data-ttu-id="49a9d-102">Свойство state (ADO)</span><span class="sxs-lookup"><span data-stu-id="49a9d-102">State property (ADO)</span></span>


<span data-ttu-id="49a9d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49a9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49a9d-104">Указывает для всех применимых объектов, открытое или закрытое состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="49a9d-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="49a9d-105">Указывает для всех применимых объектов, исполняющих асинхронный метод, независимо от того, подключен ли текущий объект, выполняется или выполняется.</span><span class="sxs-lookup"><span data-stu-id="49a9d-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="49a9d-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49a9d-106">Return value</span></span>

<span data-ttu-id="49a9d-107">Возвращает **длинное** значение, которое может быть [значением ObjectStateEnum.](objectstateenum.md)</span><span class="sxs-lookup"><span data-stu-id="49a9d-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="49a9d-108">По умолчанию значение **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="49a9d-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a9d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="49a9d-109">Remarks</span></span>

<span data-ttu-id="49a9d-110">Для определения  текущего состояния данного объекта в любое время можно использовать свойство State.</span><span class="sxs-lookup"><span data-stu-id="49a9d-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="49a9d-111">Свойство состояния **объекта** может иметь сочетание значений.</span><span class="sxs-lookup"><span data-stu-id="49a9d-111">The object's **State** property can have a combination of values.</span></span> <span data-ttu-id="49a9d-112">Например, если выполняется утверждение, это свойство будет иметь совокупное значение **adStateOpen** и **adStateExecuting.**</span><span class="sxs-lookup"><span data-stu-id="49a9d-112">For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="49a9d-113">Свойство **state** является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49a9d-113">The **State** property is read-only.</span></span>

