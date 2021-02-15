---
title: Свойство DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293688"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="bcbd4-102">Свойство DrilledDown (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-102">DrilledDown property (ADO MD)</span></span>


<span data-ttu-id="bcbd4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bcbd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bcbd4-104">Указывает, не следует ли сразу следовать за членом на оси.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="bcbd4-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bcbd4-105">Return values</span></span>

<span data-ttu-id="bcbd4-106">Возвращает значение **boolean** и является только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-106">Returns a **Boolean** value and is read-only.</span></span> <span data-ttu-id="bcbd4-107">**DrilledDown** возвращает **true,** если на оси нет других членов текущего члена.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-107">**DrilledDown** returns **True** if there are no child members of the current member on the axis.</span></span> <span data-ttu-id="bcbd4-108">**DrilledDown** возвращает **false,** если на оси имеется один или несколько членов текущего члена.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-108">**DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbd4-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="bcbd4-109">Remarks</span></span>

<span data-ttu-id="bcbd4-110">Используйте свойство **DrilledDown,** чтобы определить, есть ли по крайней мере один child этого члена на оси сразу после этого члена.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-110">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member.</span></span> <span data-ttu-id="bcbd4-111">Эти сведения полезны при отобрале участника.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-111">This information is useful when displaying the member.</span></span>

<span data-ttu-id="bcbd4-112">Это свойство поддерживается только для объектов [Member,](member-object-ado-md.md) принадлежащих [объекту Position.](position-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-112">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object.</span></span> <span data-ttu-id="bcbd4-113">Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Level.](level-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-113">An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

