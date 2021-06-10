---
title: Динамические свойства наборов записей в XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307660"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="7365d-102">Динамические свойства наборов записей в XML</span><span class="sxs-lookup"><span data-stu-id="7365d-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="7365d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7365d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7365d-104">В **формате XML** в настоящее время сохраняются следующие свойства поставщика Recordset (из клиентского cursor Engine):</span><span class="sxs-lookup"><span data-stu-id="7365d-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="7365d-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="7365d-105">**AutoRecalc**</span></span>
- <span data-ttu-id="7365d-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="7365d-106">**BatchSize**</span></span>
- <span data-ttu-id="7365d-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="7365d-107">**CommandTimeout**</span></span>
- <span data-ttu-id="7365d-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="7365d-108">**IRowsetChange**</span></span>
- <span data-ttu-id="7365d-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="7365d-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="7365d-110">**Переописываю имя**</span><span class="sxs-lookup"><span data-stu-id="7365d-110">**Reshape Name**</span></span>
- <span data-ttu-id="7365d-111">**Команда Resync**</span><span class="sxs-lookup"><span data-stu-id="7365d-111">**Resync Command**</span></span>
- <span data-ttu-id="7365d-112">**Уникальный каталог**</span><span class="sxs-lookup"><span data-stu-id="7365d-112">**Unique Catalog**</span></span>
- <span data-ttu-id="7365d-113">**Уникальная схема**</span><span class="sxs-lookup"><span data-stu-id="7365d-113">**Unique Schema**</span></span>
- <span data-ttu-id="7365d-114">**Уникальная таблица**</span><span class="sxs-lookup"><span data-stu-id="7365d-114">**Unique Table**</span></span>
- <span data-ttu-id="7365d-115">**Обновление Resync**</span><span class="sxs-lookup"><span data-stu-id="7365d-115">**Update Resync**</span></span>
- <span data-ttu-id="7365d-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="7365d-116">**UpdateCriteria**</span></span>


<span data-ttu-id="7365d-117">Эти свойства сохраняются в разделе схемы в качестве атрибутов определения элемента для сохраняемого **наборов** записей.</span><span class="sxs-lookup"><span data-stu-id="7365d-117">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted.</span></span> <span data-ttu-id="7365d-118">Эти атрибуты определяются в пространстве имен схемы rowset и должны иметь префикс "rs:".</span><span class="sxs-lookup"><span data-stu-id="7365d-118">These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="7365d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7365d-119">See also</span></span>

- [<span data-ttu-id="7365d-120">Динамические свойства ADO</span><span class="sxs-lookup"><span data-stu-id="7365d-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
