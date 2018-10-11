---
title: Recordset Dynamic Properties in XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480104"
---
# <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="9fd64-102">Recordset Dynamic Properties in XML</span><span class="sxs-lookup"><span data-stu-id="9fd64-102">Recordset Dynamic Properties in XML</span></span>


<span data-ttu-id="9fd64-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fd64-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="recordset-dynamic-properties-in-xml"></a><span data-ttu-id="9fd64-104">Recordset Dynamic Properties in XML</span><span class="sxs-lookup"><span data-stu-id="9fd64-104">Recordset Dynamic Properties in XML</span></span>

<span data-ttu-id="9fd64-105">Следующие свойства от поставщика **набора записей** (от обработчика курсор клиента) в настоящее время, сохраняются в формате XML:</span><span class="sxs-lookup"><span data-stu-id="9fd64-105">The following **Recordset** provider-specific properties (from the Client Cursor Engine) are currently persisted into the XML format:</span></span>

  - <span data-ttu-id="9fd64-106">**Обновление повторной синхронизации**</span><span class="sxs-lookup"><span data-stu-id="9fd64-106">**Update Resync**</span></span>

  - <span data-ttu-id="9fd64-107">**Уникальная таблица**</span><span class="sxs-lookup"><span data-stu-id="9fd64-107">**Unique Table**</span></span>

  - <span data-ttu-id="9fd64-108">**Уникальный схемы**</span><span class="sxs-lookup"><span data-stu-id="9fd64-108">**Unique Schema**</span></span>

  - <span data-ttu-id="9fd64-109">**Уникальный каталога**</span><span class="sxs-lookup"><span data-stu-id="9fd64-109">**Unique Catalog**</span></span>

  - <span data-ttu-id="9fd64-110">**Команда синхронизации**</span><span class="sxs-lookup"><span data-stu-id="9fd64-110">**Resync Command**</span></span>

  - <span data-ttu-id="9fd64-111">**IRowsetChange**</span><span class="sxs-lookup"><span data-stu-id="9fd64-111">**IRowsetChange**</span></span>

  - <span data-ttu-id="9fd64-112">**IRowsetUpdate**</span><span class="sxs-lookup"><span data-stu-id="9fd64-112">**IRowsetUpdate**</span></span>

  - <span data-ttu-id="9fd64-113">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="9fd64-113">**CommandTimeout**</span></span>

  - <span data-ttu-id="9fd64-114">**Размер пакета**</span><span class="sxs-lookup"><span data-stu-id="9fd64-114">**BatchSize**</span></span>

  - <span data-ttu-id="9fd64-115">**UpdateCriteria**</span><span class="sxs-lookup"><span data-stu-id="9fd64-115">**UpdateCriteria**</span></span>

  - <span data-ttu-id="9fd64-116">**Изменить форму имя**</span><span class="sxs-lookup"><span data-stu-id="9fd64-116">**Reshape Name**</span></span>

  - <span data-ttu-id="9fd64-117">**AutoRecalc**</span><span class="sxs-lookup"><span data-stu-id="9fd64-117">**AutoRecalc**</span></span>

<span data-ttu-id="9fd64-118">Эти свойства сохраняются в разделе схемы как атрибуты определения элемента для **набора записей** , сохраняется.</span><span class="sxs-lookup"><span data-stu-id="9fd64-118">These properties are saved in the schema section as attributes of the element definition for the **Recordset** being persisted.</span></span> <span data-ttu-id="9fd64-119">Эти атрибуты определены в пространстве имен схемы строк и должен иметь префикс «rs:».</span><span class="sxs-lookup"><span data-stu-id="9fd64-119">These attributes are defined in the rowset schema namespace and must have the prefix "rs:".</span></span>

