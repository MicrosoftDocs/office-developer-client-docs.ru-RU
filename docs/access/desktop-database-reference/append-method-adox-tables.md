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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297076"
---
# <a name="append-method-adox-tables"></a><span data-ttu-id="5d842-102">Метод Append (коллекция Tables в ADOX)</span><span class="sxs-lookup"><span data-stu-id="5d842-102">Append method (ADOX Tables)</span></span>

<span data-ttu-id="5d842-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d842-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d842-104">Добавляет новый объект [Table](table-object-adox.md) в коллекцию [Tables](tables-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="5d842-104">Adds a new [Table](table-object-adox.md) object to the [Tables](tables-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d842-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d842-105">Syntax</span></span>

<span data-ttu-id="5d842-106">*Таблицы*. Добавление*таблицы*</span><span class="sxs-lookup"><span data-stu-id="5d842-106">*Tables*.Append*Table*</span></span>

## <a name="parameters"></a><span data-ttu-id="5d842-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d842-107">Parameters</span></span>

|<span data-ttu-id="5d842-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d842-108">Parameter</span></span>|<span data-ttu-id="5d842-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5d842-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5d842-110">*Table*</span><span class="sxs-lookup"><span data-stu-id="5d842-110">*Table*</span></span> | <span data-ttu-id="5d842-111">Значение **Variant** , которое содержит ссылку на **таблицу** для добавления или имя таблицы для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="5d842-111">A **Variant** value that contains a reference to the **Table** to append or the name of the table to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5d842-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d842-112">Remarks</span></span>

<span data-ttu-id="5d842-113">Если поставщик не поддерживает создание таблиц, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="5d842-113">An error will occur if the provider does not support creating tables.</span></span>

