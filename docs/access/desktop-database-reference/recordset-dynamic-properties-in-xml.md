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
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="1ad18-102">Динамические свойства наборов записей в XML</span><span class="sxs-lookup"><span data-stu-id="1ad18-102">Recordset dynamic properties in XML</span></span>

<span data-ttu-id="1ad18-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ad18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ad18-104">Следующие свойства, зависящие от поставщика **набора записей** (из обработчика курсоров клиента), в настоящее время сохраняются в формате XML:</span><span class="sxs-lookup"><span data-stu-id="1ad18-104">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

- <span data-ttu-id="1ad18-105">**Ауторекалк**</span><span class="sxs-lookup"><span data-stu-id="1ad18-105">**AutoRecalc**</span></span>
- <span data-ttu-id="1ad18-106">**BatchSize**</span><span class="sxs-lookup"><span data-stu-id="1ad18-106">**BatchSize**</span></span>
- <span data-ttu-id="1ad18-107">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="1ad18-107">**CommandTimeout**</span></span>
- <span data-ttu-id="1ad18-108">**Ировсетчанже**</span><span class="sxs-lookup"><span data-stu-id="1ad18-108">**IRowsetChange**</span></span>
- <span data-ttu-id="1ad18-109">**Ировсетупдате**</span><span class="sxs-lookup"><span data-stu-id="1ad18-109">**IRowsetUpdate**</span></span>
- <span data-ttu-id="1ad18-110">**Изменение имени фигуры**</span><span class="sxs-lookup"><span data-stu-id="1ad18-110">**Reshape Name**</span></span>
- <span data-ttu-id="1ad18-111">**Команда Resync**</span><span class="sxs-lookup"><span data-stu-id="1ad18-111">**Resync Command**</span></span>
- <span data-ttu-id="1ad18-112">**Уникальный каталог**</span><span class="sxs-lookup"><span data-stu-id="1ad18-112">**Unique Catalog**</span></span>
- <span data-ttu-id="1ad18-113">**Уникальная схема**</span><span class="sxs-lookup"><span data-stu-id="1ad18-113">**Unique Schema**</span></span>
- <span data-ttu-id="1ad18-114">**Уникальная таблица**</span><span class="sxs-lookup"><span data-stu-id="1ad18-114">**Unique Table**</span></span>
- <span data-ttu-id="1ad18-115">**Повторная синхронизация обновлений**</span><span class="sxs-lookup"><span data-stu-id="1ad18-115">**Update Resync**</span></span>
- <span data-ttu-id="1ad18-116">**Упдатекритериа**</span><span class="sxs-lookup"><span data-stu-id="1ad18-116">**UpdateCriteria**</span></span>


<span data-ttu-id="1ad18-117">Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для сохраняемого **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1ad18-117">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted.</span></span> <span data-ttu-id="1ad18-118">Эти атрибуты определены в пространстве имен схемы набора строк и должны иметь префикс "RS:".</span><span class="sxs-lookup"><span data-stu-id="1ad18-118">These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

## <a name="see-also"></a><span data-ttu-id="1ad18-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1ad18-119">See also</span></span>

- [<span data-ttu-id="1ad18-120">Динамические свойства ADO</span><span class="sxs-lookup"><span data-stu-id="1ad18-120">ADO dynamic properties</span></span>](ado-dynamic-properties.md)
