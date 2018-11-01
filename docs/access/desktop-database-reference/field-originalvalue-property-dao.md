---
title: Field.OriginalValue Property (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ead15a227ccd3ff7d77796aea4d23d776652be86
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873070"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="a7310-102">Field.OriginalValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7310-102">Field.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="a7310-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7310-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a7310-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7310-104">Syntax</span></span>

<span data-ttu-id="a7310-105">*выражение* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="a7310-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="a7310-106">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="a7310-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7310-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7310-107">Remarks</span></span>

<span data-ttu-id="a7310-108">Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="a7310-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="a7310-109">Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** .</span><span class="sxs-lookup"><span data-stu-id="a7310-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="a7310-110">Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт.</span><span class="sxs-lookup"><span data-stu-id="a7310-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="a7310-111">В этом случае будет доступен через свойство **[VisibleValue](field-visiblevalue-property-dao.md)** новое значение в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a7310-111">When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

