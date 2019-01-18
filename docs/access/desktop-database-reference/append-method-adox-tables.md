---
title: Метод Append (коллекция Tables в ADOX)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2bf2479c2a34291f245783ebaecd75ba31d2ac8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706060"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="b16a1-102">Метод Append (коллекция Tables в ADOX)</span><span class="sxs-lookup"><span data-stu-id="b16a1-102">Append method (ADOX Tables)</span></span>

<span data-ttu-id="b16a1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b16a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b16a1-104">Добавляет новый объект [таблицы](table-object-adox.md) в коллекцию [таблиц](tables-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="b16a1-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b16a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b16a1-105">Syntax</span></span>

<span data-ttu-id="b16a1-106">*Таблицы*. Добавление*таблицы*</span><span class="sxs-lookup"><span data-stu-id="b16a1-106">*Tables*.Append*Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="b16a1-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b16a1-107">Parameters</span></span>

|<span data-ttu-id="b16a1-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b16a1-108">Parameter</span></span>|<span data-ttu-id="b16a1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b16a1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b16a1-110">*Table*</span><span class="sxs-lookup"><span data-stu-id="b16a1-110">*Table*</span></span> | <span data-ttu-id="b16a1-111">Значение **типа Variant** , содержащий ссылку на **таблицу** для добавления или имя таблицы для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="b16a1-111">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b16a1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b16a1-112">Remarks</span></span>

<span data-ttu-id="b16a1-113">Если поставщик не поддерживает создание таблиц, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b16a1-113">An error will occur if the provider does not support creating tables.</span></span>

