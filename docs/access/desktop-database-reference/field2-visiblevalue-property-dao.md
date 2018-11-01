---
title: Field2.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 896cc3866b52aeb8bbd2956ea84f9470671a407a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873259"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="e7202-102">Field2.VisibleValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e7202-102">Field2.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="e7202-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7202-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="e7202-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7202-104">Syntax</span></span>

<span data-ttu-id="e7202-105">*выражение* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="e7202-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="e7202-106">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="e7202-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7202-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7202-107">Remarks</span></span>

<span data-ttu-id="e7202-108">Это свойство содержит значение поля, который в данный момент в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="e7202-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="e7202-109">Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="e7202-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="e7202-110">В этом случае значение, которое задано второй клиента будет доступен через это свойство.</span><span class="sxs-lookup"><span data-stu-id="e7202-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

