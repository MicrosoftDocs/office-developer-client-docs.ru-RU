---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ef77f5882f4b215764a82d343d59f1f31487e58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886118"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="fc40f-102">TableDef.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc40f-102">TableDef.RecordCount Property (DAO)</span></span>


<span data-ttu-id="fc40f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc40f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc40f-104">Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="fc40f-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="fc40f-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="fc40f-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc40f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc40f-106">Syntax</span></span>

<span data-ttu-id="fc40f-107">*выражение* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="fc40f-107">*expression* .RecordCount</span></span>

<span data-ttu-id="fc40f-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="fc40f-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc40f-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc40f-109">Remarks</span></span>

<span data-ttu-id="fc40f-110">Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.</span><span class="sxs-lookup"><span data-stu-id="fc40f-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="fc40f-111">При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.</span><span class="sxs-lookup"><span data-stu-id="fc40f-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

