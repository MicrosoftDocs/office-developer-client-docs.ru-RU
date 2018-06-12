---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808259"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="77d95-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="77d95-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="77d95-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77d95-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77d95-105">Освобождает служебной программы функций, вызываемых явным образом с помощью функции [ScInitMapiUtil](scinitmapiutil.md) или неявно с помощью функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="77d95-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77d95-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="77d95-106">Header file:</span></span>  <br/> |<span data-ttu-id="77d95-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="77d95-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="77d95-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="77d95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="77d95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="77d95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="77d95-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="77d95-110">Called by:</span></span>  <br/> |<span data-ttu-id="77d95-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="77d95-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="77d95-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="77d95-112">Parameters</span></span>

<span data-ttu-id="77d95-113">Нет</span><span class="sxs-lookup"><span data-stu-id="77d95-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="77d95-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="77d95-114">Return value</span></span>

<span data-ttu-id="77d95-115">Нет</span><span class="sxs-lookup"><span data-stu-id="77d95-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="77d95-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="77d95-116">Remarks</span></span>

<span data-ttu-id="77d95-117">Функция **DeinitMapiUtil** release функции инициализации с [ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="77d95-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="77d95-118">По завершении работы функций, вызываемых **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их.</span><span class="sxs-lookup"><span data-stu-id="77d95-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="77d95-119">С другой стороны [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="77d95-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

