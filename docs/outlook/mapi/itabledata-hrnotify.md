---
title: Итабледатахрнотифи
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
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413271"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="b035a-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="b035a-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="b035a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b035a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b035a-105">Отправляет уведомление для строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="b035a-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="b035a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b035a-106">Parameters</span></span>

 <span data-ttu-id="b035a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b035a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b035a-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="b035a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b035a-109">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="b035a-109">_cValues_</span></span>
  
> <span data-ttu-id="b035a-110">возврата Количество значений свойств в структуре [спропвалуе](spropvalue.md) , на которую указывает параметр _лпспропвалуе_ .</span><span class="sxs-lookup"><span data-stu-id="b035a-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="b035a-111">_Лпспропвалуе_</span><span class="sxs-lookup"><span data-stu-id="b035a-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="b035a-112">возврата Указатель на структуру **спропвалуе** , которая описывает значения столбцов в целевой строке.</span><span class="sxs-lookup"><span data-stu-id="b035a-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b035a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b035a-113">Return value</span></span>

<span data-ttu-id="b035a-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b035a-114">S_OK</span></span> 
  
> <span data-ttu-id="b035a-115">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b035a-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b035a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b035a-116">Remarks</span></span>

<span data-ttu-id="b035a-117">Метод **итабледата:: хрнотифи** ОТПРАВЛЯЕТ уведомление табле_ров_модифиед для строки, которая соответствует строке, описываемой свойствами, на которые указывает параметр _лпспропвалуе_ .</span><span class="sxs-lookup"><span data-stu-id="b035a-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="b035a-118">**Хрнотифи** отправляет уведомление независимо от того, были ли внесены изменения в строку.</span><span class="sxs-lookup"><span data-stu-id="b035a-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="b035a-119">Все клиенты и поставщики услуг, имеющие представления таблицы и вызываемые с помощью метода [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений в своих представлениях, получат это уведомление.</span><span class="sxs-lookup"><span data-stu-id="b035a-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b035a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b035a-120">See also</span></span>



[<span data-ttu-id="b035a-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b035a-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="b035a-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b035a-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b035a-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b035a-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

