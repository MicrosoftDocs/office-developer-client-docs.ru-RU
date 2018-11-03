---
title: Динамические свойства наборов записей в XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946960"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="28061-102">Динамические свойства наборов записей в XML</span><span class="sxs-lookup"><span data-stu-id="28061-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="28061-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28061-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28061-104">Следующие свойства от поставщика **набора записей** (от обработчика курсор клиента) в настоящее время, сохраняются в формате XML:</span><span class="sxs-lookup"><span data-stu-id="28061-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="28061-105">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="28061-105">**AutoRecalc**</span></span>
- <span data-ttu-id="28061-106">**Размер пакета**</span><span class="sxs-lookup"><span data-stu-id="28061-106">**BatchSize**</span></span>
- <span data-ttu-id="28061-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="28061-107">**CommandTimeout**</span></span>
- <span data-ttu-id="28061-108">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="28061-108">**IRowsetChange**</span></span>
- <span data-ttu-id="28061-109">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="28061-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="28061-110">**Изменить форму имя**</span><span class="sxs-lookup"><span data-stu-id="28061-110">**Reshape Name**</span></span>
- <span data-ttu-id="28061-111">**Команда синхронизации**</span><span class="sxs-lookup"><span data-stu-id="28061-111">**Resync Command**</span></span>
- <span data-ttu-id="28061-112">**Уникальный каталога**</span><span class="sxs-lookup"><span data-stu-id="28061-112">**Unique Catalog**</span></span>
- <span data-ttu-id="28061-113">**Уникальный схемы**</span><span class="sxs-lookup"><span data-stu-id="28061-113">**Unique Schema**</span></span>
- <span data-ttu-id="28061-114">**Уникальная таблица**</span><span class="sxs-lookup"><span data-stu-id="28061-114">**Unique Table**</span></span>
- <span data-ttu-id="28061-115">**Обновление повторной синхронизации**</span><span class="sxs-lookup"><span data-stu-id="28061-115">**Update Resync**</span></span>
- <span data-ttu-id="28061-116">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="28061-116">**UpdateCriteria**</span></span>


<span data-ttu-id="28061-117">Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для **набора записей** , сохраняется.</span><span class="sxs-lookup"><span data-stu-id="28061-117">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted.</span></span> <span data-ttu-id="28061-118">Эти атрибуты определены в пространстве имен схемы строк и должен иметь префикс «rs:».</span><span class="sxs-lookup"><span data-stu-id="28061-118">These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="28061-119">См. также</span><span class="sxs-lookup"><span data-stu-id="28061-119">See also</span></span>

- [<span data-ttu-id="28061-120">Динамические свойства ADO</span><span class="sxs-lookup"><span data-stu-id="28061-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)