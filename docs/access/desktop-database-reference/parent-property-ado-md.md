---
title: Parent property (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287792"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="725b7-102">Parent property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="725b7-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="725b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="725b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="725b7-104">Указывает член, который является родительским для текущего члена в иерархии.</span><span class="sxs-lookup"><span data-stu-id="725b7-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="725b7-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="725b7-105">Return values</span></span>

<span data-ttu-id="725b7-106">Возвращает объект [Member](member-object-ado-md.md) и является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="725b7-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="725b7-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="725b7-107">Remarks</span></span>

<span data-ttu-id="725b7-108">У члена, который находится на верхнем уровне иерархии (корневой) нет родительского.</span><span class="sxs-lookup"><span data-stu-id="725b7-108">A member that is at the top level of a hierarchy (the root) has no parent.</span></span> <span data-ttu-id="725b7-109">Это свойство поддерживается только для объектов **Member,** принадлежащих [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="725b7-109">This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="725b7-110">Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="725b7-110">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

