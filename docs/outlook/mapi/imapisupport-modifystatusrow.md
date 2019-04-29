---
title: Имаписуппортмодифистатусров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417163"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="735da-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="735da-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="735da-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="735da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="735da-105">Изменяет таблицу состояний, добавляя новую строку или изменяя существующую строку.</span><span class="sxs-lookup"><span data-stu-id="735da-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="735da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="735da-106">Parameters</span></span>

 <span data-ttu-id="735da-107">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="735da-107">_cValues_</span></span>
  
> <span data-ttu-id="735da-108">возврата Количество свойств, которые необходимо включить в строку таблицы "Создание или изменение состояния".</span><span class="sxs-lookup"><span data-stu-id="735da-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="735da-109">_Лпколумнвалс_</span><span class="sxs-lookup"><span data-stu-id="735da-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="735da-110">возврата Указатель на массив значений свойств, описывающих свойства, которые необходимо включить в качестве столбцов в строку "Новая или измененная таблица состояний".</span><span class="sxs-lookup"><span data-stu-id="735da-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="735da-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="735da-111">_ulFlags_</span></span>
  
> <span data-ttu-id="735da-112">возврата Битовая маска флагов, определяющих, как обрабатывается информация, определяющая строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="735da-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="735da-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="735da-113">The following flag can be set:</span></span>
    
<span data-ttu-id="735da-114">СТАТУСРОВ_УПДАТЕ</span><span class="sxs-lookup"><span data-stu-id="735da-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="735da-115">Направляет интерфейс MAPI для объединения свойств, включенных в массив, на который указывает _лпколумнвалс_ , с существующей строкой таблицы состояний, а не в новой строке.</span><span class="sxs-lookup"><span data-stu-id="735da-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="735da-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="735da-116">Return value</span></span>

<span data-ttu-id="735da-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="735da-117">S_OK</span></span> 
  
> <span data-ttu-id="735da-118">Таблица состояния успешно обновлена.</span><span class="sxs-lookup"><span data-stu-id="735da-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="735da-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="735da-119">Remarks</span></span>

<span data-ttu-id="735da-120">Метод **имаписуппорт:: модифистатусров** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="735da-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="735da-121">Поставщики услуг вызывают **модифистатусров** во время входа, чтобы добавить строку в таблицу состояния и в другое время сеанса, чтобы обновить строку.</span><span class="sxs-lookup"><span data-stu-id="735da-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="735da-122">**Модифистатусров** предоставляет MAPI со сведениями, необходимыми для создания таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="735da-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="735da-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="735da-123">Notes to callers</span></span>

<span data-ttu-id="735da-124">Установите флаг СТАТУСРОВ_УПДАТЕ при вызове **модифистатусров** для внесения изменений в свойства в существующей строке таблицы состояний.</span><span class="sxs-lookup"><span data-stu-id="735da-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="735da-125">Это информирует MAPI, что в параметре _лпколумнвалс_ передаются только изменяемые столбцы.</span><span class="sxs-lookup"><span data-stu-id="735da-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="735da-126">Клиенты могут использовать сведения из таблицы состояния для доступа к объекту Status.</span><span class="sxs-lookup"><span data-stu-id="735da-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="735da-127">Полный список столбцов, которые необходимо включить в строку таблицы состояния, представлен в статье [Status](status-tables.md)Tables.</span><span class="sxs-lookup"><span data-stu-id="735da-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="735da-128">См. также</span><span class="sxs-lookup"><span data-stu-id="735da-128">See also</span></span>



[<span data-ttu-id="735da-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="735da-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

