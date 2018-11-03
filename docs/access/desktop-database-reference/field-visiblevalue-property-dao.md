---
title: Свойство Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 461b8c43bf9000e5ecde3a3676cebf54be8e4166
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927573"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="6ee6a-102">Свойство Field.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ee6a-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="6ee6a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ee6a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee6a-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee6a-104">Syntax</span></span>

<span data-ttu-id="6ee6a-105">*выражение* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="6ee6a-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="6ee6a-106">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="6ee6a-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee6a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ee6a-107">Remarks</span></span>

<span data-ttu-id="6ee6a-108">Это свойство содержит значение поля, который в данный момент в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="6ee6a-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="6ee6a-109">Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="6ee6a-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="6ee6a-110">В этом случае значение, которое задано второй клиента будет доступен через это свойство.</span><span class="sxs-lookup"><span data-stu-id="6ee6a-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

