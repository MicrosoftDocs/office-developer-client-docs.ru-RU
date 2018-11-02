---
title: Свойство TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920923"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="d9913-102">Свойство TableDef.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="d9913-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="d9913-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9913-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9913-104">Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="d9913-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="d9913-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="d9913-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9913-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9913-106">Syntax</span></span>

<span data-ttu-id="d9913-107">*выражение* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="d9913-107">*expression* .RecordCount</span></span>

<span data-ttu-id="d9913-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="d9913-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9913-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9913-109">Remarks</span></span>

<span data-ttu-id="d9913-110">Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.</span><span class="sxs-lookup"><span data-stu-id="d9913-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="d9913-111">При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.</span><span class="sxs-lookup"><span data-stu-id="d9913-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>

