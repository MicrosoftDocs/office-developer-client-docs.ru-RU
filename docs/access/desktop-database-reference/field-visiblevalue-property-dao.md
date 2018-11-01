---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462359ca02b4a5724c781da303b13a97c73be388
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871208"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="9dd76-102">Field.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9dd76-102">Field.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="9dd76-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9dd76-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd76-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd76-104">Syntax</span></span>

<span data-ttu-id="9dd76-105">*выражение* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="9dd76-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="9dd76-106">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="9dd76-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd76-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9dd76-107">Remarks</span></span>

<span data-ttu-id="9dd76-108">Это свойство содержит значение поля, который в данный момент в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="9dd76-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="9dd76-109">Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="9dd76-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="9dd76-110">В этом случае значение, которое задано второй клиента будет доступен через это свойство.</span><span class="sxs-lookup"><span data-stu-id="9dd76-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

