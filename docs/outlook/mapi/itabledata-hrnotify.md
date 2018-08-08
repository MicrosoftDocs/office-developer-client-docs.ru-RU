---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809611"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="2c13a-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="2c13a-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="2c13a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c13a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c13a-105">Отправляет уведомления для строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="2c13a-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="2c13a-106">���������</span><span class="sxs-lookup"><span data-stu-id="2c13a-106">Parameters</span></span>

 <span data-ttu-id="2c13a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c13a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2c13a-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="2c13a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2c13a-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="2c13a-109">_cValues_</span></span>
  
> <span data-ttu-id="2c13a-110">[in] Число значений свойств в структуре [SPropValue](spropvalue.md) указывает параметр _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="2c13a-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="2c13a-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="2c13a-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="2c13a-112">[in] Указатель на структуру **SPropValue** , описаны значения столбцов в строки целевое значение.</span><span class="sxs-lookup"><span data-stu-id="2c13a-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2c13a-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2c13a-113">Return value</span></span>

<span data-ttu-id="2c13a-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2c13a-114">S_OK</span></span> 
  
> <span data-ttu-id="2c13a-115">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2c13a-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c13a-116">���������</span><span class="sxs-lookup"><span data-stu-id="2c13a-116">Remarks</span></span>

<span data-ttu-id="2c13a-117">Метод **ITableData::HrNotify** отправляет уведомление TABLE_ROW_MODIFIED для строки, которая соответствует строке, описываемого свойства, на который указывает параметр _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="2c13a-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="2c13a-118">**HrNotify** отправляет уведомление, независимо от того, является ли изменений в строку.</span><span class="sxs-lookup"><span data-stu-id="2c13a-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="2c13a-119">Все клиенты и поставщиков услуг, которые имеют представления таблицы и вызова [IMAPITable::Advise](imapitable-advise.md) для регистрации уведомлений на их представления получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="2c13a-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c13a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2c13a-120">See also</span></span>



[<span data-ttu-id="2c13a-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2c13a-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2c13a-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2c13a-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="2c13a-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c13a-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

