---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481562"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="319e8-102">TableDef.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="319e8-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="319e8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="319e8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="319e8-104">Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="319e8-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="319e8-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="319e8-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="319e8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="319e8-106">Syntax</span></span>

<span data-ttu-id="319e8-107">*выражение* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="319e8-107">*expression* .RecordCount</span></span>

<span data-ttu-id="319e8-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="319e8-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="319e8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="319e8-109">Remarks</span></span>

<span data-ttu-id="319e8-110">Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.</span><span class="sxs-lookup"><span data-stu-id="319e8-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="319e8-111">При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.</span><span class="sxs-lookup"><span data-stu-id="319e8-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

