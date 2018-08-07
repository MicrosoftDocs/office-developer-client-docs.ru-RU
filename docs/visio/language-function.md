---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Позволяет выполнять операции сравнения между представлениями другой язык. Она лучше всего использовать для преобразования значений тегов (BCP 47) язык Internet инженерной рабочей группы в значения id (LCID) для языкового стандарта.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814052"
---
# <a name="language-function"></a><span data-ttu-id="9cc04-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="9cc04-104">LANGUAGE Function</span></span>

<span data-ttu-id="9cc04-105">Позволяет выполнять операции сравнения между представлениями другой язык.</span><span class="sxs-lookup"><span data-stu-id="9cc04-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="9cc04-106">Она лучше всего использовать для преобразования значений тегов (BCP 47) язык Internet инженерной рабочей группы в значения id (LCID) для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="9cc04-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="9cc04-107">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="9cc04-107">Version Information</span></span>

<span data-ttu-id="9cc04-108">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="9cc04-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9cc04-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cc04-109">Syntax</span></span>

 <span data-ttu-id="9cc04-110">**Язык** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="9cc04-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="9cc04-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cc04-111">Parameters</span></span>

|<span data-ttu-id="9cc04-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9cc04-112">**Name**</span></span>|<span data-ttu-id="9cc04-113">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="9cc04-113">**Required/Optional**</span></span>|<span data-ttu-id="9cc04-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9cc04-114">**Data Type**</span></span>|<span data-ttu-id="9cc04-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9cc04-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9cc04-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="9cc04-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="9cc04-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9cc04-117">Required</span></span>  <br/> |<span data-ttu-id="9cc04-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="9cc04-118">**String**</span></span> <br/> |<span data-ttu-id="9cc04-119">Код языка или BCP 47 значение языка.</span><span class="sxs-lookup"><span data-stu-id="9cc04-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="9cc04-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9cc04-120">Return value</span></span>

<span data-ttu-id="9cc04-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="9cc04-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="9cc04-122">Пример</span><span class="sxs-lookup"><span data-stu-id="9cc04-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="9cc04-123">Возвращает значение "1033".</span><span class="sxs-lookup"><span data-stu-id="9cc04-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="9cc04-124">Возвращает значение "3082".</span><span class="sxs-lookup"><span data-stu-id="9cc04-124">Returns a value of '3082'.</span></span>
  

