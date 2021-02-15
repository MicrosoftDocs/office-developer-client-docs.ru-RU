---
title: Свойство ParentSameAsPrev (ADO MD)
TOCTitle: ParentSameAsPrev property (ADO MD)
ms:assetid: 0f53a064-f63f-172e-d17f-1a3335c47ab5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248863(v=office.15)
ms:contentKeyID: 48543263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b9f7157dc0f7805f2b10470c00d35f26977584d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287733"
---
# <a name="parentsameasprev-property-ado-md"></a><span data-ttu-id="be1c3-102">Свойство ParentSameAsPrev (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="be1c3-102">ParentSameAsPrev property (ADO MD)</span></span>


<span data-ttu-id="be1c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be1c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be1c3-104">Указывает, является ли родительский член этой позиции тем же, что и родительский член непосредственного предыдущего.</span><span class="sxs-lookup"><span data-stu-id="be1c3-104">Indicates whether the parent of this position member is the same as the parent of the immediately preceding member.</span></span>

## <a name="return-values"></a><span data-ttu-id="be1c3-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="be1c3-105">Return values</span></span>

<span data-ttu-id="be1c3-106">Возвращает значение **boolean** и является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be1c3-106">Returns a **Boolean** value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1c3-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="be1c3-107">Remarks</span></span>

<span data-ttu-id="be1c3-108">Это свойство поддерживается только для объектов [Member,](member-object-ado-md.md) принадлежащих [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="be1c3-108">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object.</span></span> <span data-ttu-id="be1c3-109">Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="be1c3-109">An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

