---
title: Свойство Field2.VisibleValue (DAO)
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
ms.openlocfilehash: 9b33fe61eaeb7d1a6006ffaf4566b65be9f68243
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926068"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="c06de-102">Свойство Field2.VisibleValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="c06de-102">Field2.VisibleValue property (DAO)</span></span>


<span data-ttu-id="c06de-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c06de-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c06de-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c06de-104">Syntax</span></span>

<span data-ttu-id="c06de-105">*выражение* . VisibleValue</span><span class="sxs-lookup"><span data-stu-id="c06de-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="c06de-106">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="c06de-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c06de-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="c06de-107">Remarks</span></span>

<span data-ttu-id="c06de-108">Это свойство содержит значение поля, который в данный момент в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="c06de-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="c06de-109">Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="c06de-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="c06de-110">В этом случае значение, которое задано второй клиента будет доступен через это свойство.</span><span class="sxs-lookup"><span data-stu-id="c06de-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

