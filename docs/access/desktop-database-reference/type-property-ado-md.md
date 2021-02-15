---
title: Свойство Type (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99b4e3e2c6930d8162c57d75978e9dba7b5af3e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313988"
---
# <a name="type-property-ado-md"></a><span data-ttu-id="63df8-102">Свойство Type (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="63df8-102">Type property (ADO MD)</span></span>


<span data-ttu-id="63df8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63df8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63df8-104">Указывает тип текущего члена.</span><span class="sxs-lookup"><span data-stu-id="63df8-104">Indicates the type of the current member.</span></span>

## <a name="return-values"></a><span data-ttu-id="63df8-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="63df8-105">Return values</span></span>

<span data-ttu-id="63df8-106">Возвращает значение [MemberTypeEnum](membertypeenum.md) и является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63df8-106">Returns a [MemberTypeEnum](membertypeenum.md) value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="63df8-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="63df8-107">Remarks</span></span>

<span data-ttu-id="63df8-108">Это свойство поддерживается только для объектов [Member,](member-object-ado-md.md) принадлежащих [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="63df8-108">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="63df8-109">Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="63df8-109">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

