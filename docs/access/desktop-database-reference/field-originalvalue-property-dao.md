---
title: Свойство Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d850ebcfef6ea2c08e20ed953dfcc7b5ea23cbab
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926796"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="5c0b4-102">Свойство Field.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c0b4-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="5c0b4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c0b4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="5c0b4-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c0b4-104">Syntax</span></span>

<span data-ttu-id="5c0b4-105">*выражение* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="5c0b4-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="5c0b4-106">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="5c0b4-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c0b4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c0b4-107">Remarks</span></span>

<span data-ttu-id="5c0b4-108">Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="5c0b4-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="5c0b4-109">Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** .</span><span class="sxs-lookup"><span data-stu-id="5c0b4-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="5c0b4-110">Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт.</span><span class="sxs-lookup"><span data-stu-id="5c0b4-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="5c0b4-111">В этом случае будет доступен через свойство **[VisibleValue](field-visiblevalue-property-dao.md)** новое значение в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5c0b4-111">When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

