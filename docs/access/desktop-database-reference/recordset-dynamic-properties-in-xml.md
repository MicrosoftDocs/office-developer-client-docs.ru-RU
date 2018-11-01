---
title: Свойства динамической записей в формате XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884263"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="e5577-102">Свойства динамической записей в формате XML</span><span class="sxs-lookup"><span data-stu-id="e5577-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="e5577-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5577-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="e5577-104">Свойства динамической записей в формате XML</span><span class="sxs-lookup"><span data-stu-id="e5577-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="e5577-105">Следующие свойства от поставщика **набора записей** (от обработчика курсор клиента) в настоящее время, сохраняются в формате XML:</span><span class="sxs-lookup"><span data-stu-id="e5577-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="e5577-106">**Обновление повторной синхронизации**</span><span class="sxs-lookup"><span data-stu-id="e5577-106">**Update Resync**</span></span>

  - <span data-ttu-id="e5577-107">**Уникальная таблица**</span><span class="sxs-lookup"><span data-stu-id="e5577-107">**Unique Table**</span></span>

  - <span data-ttu-id="e5577-108">**Уникальный схемы**</span><span class="sxs-lookup"><span data-stu-id="e5577-108">**Unique Schema**</span></span>

  - <span data-ttu-id="e5577-109">**Уникальный каталога**</span><span class="sxs-lookup"><span data-stu-id="e5577-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="e5577-110">**Команда синхронизации**</span><span class="sxs-lookup"><span data-stu-id="e5577-110">**Resync Command**</span></span>

  - <span data-ttu-id="e5577-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="e5577-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="e5577-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="e5577-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="e5577-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="e5577-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="e5577-114">**Размер пакета**</span><span class="sxs-lookup"><span data-stu-id="e5577-114">**BatchSize**</span></span>

  - <span data-ttu-id="e5577-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="e5577-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="e5577-116">**Изменить форму имя**</span><span class="sxs-lookup"><span data-stu-id="e5577-116">**Reshape Name**</span></span>

  - <span data-ttu-id="e5577-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="e5577-117">**AutoRecalc**</span></span>

<span data-ttu-id="e5577-118">Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для **набора записей** , сохраняется.</span><span class="sxs-lookup"><span data-stu-id="e5577-118">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted.</span></span> <span data-ttu-id="e5577-119">Эти атрибуты определены в пространстве имен схемы строк и должен иметь префикс «rs:».</span><span class="sxs-lookup"><span data-stu-id="e5577-119">These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

