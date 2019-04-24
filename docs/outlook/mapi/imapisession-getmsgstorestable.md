---
title: Имаписессионжетмсгсторестабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338831"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="c1432-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="c1432-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="c1432-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1432-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1432-105">Предоставляет доступ к таблице хранилища сообщений, в которой содержатся сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="c1432-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c1432-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1432-106">Parameters</span></span>

 <span data-ttu-id="c1432-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1432-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c1432-108">возврата Битовая маска флагов, определяющих формат столбцов, которые являются символьными строками.</span><span class="sxs-lookup"><span data-stu-id="c1432-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="c1432-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c1432-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c1432-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1432-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c1432-111">Строковые столбцы представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c1432-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="c1432-112">Если флаг МАПИ_УНИКОДЕ не установлен, строковые столбцы представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c1432-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="c1432-113">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="c1432-113">_lppTable_</span></span>
  
> <span data-ttu-id="c1432-114">вышли Указатель на указатель на таблицу хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1432-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1432-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1432-115">Return value</span></span>

<span data-ttu-id="c1432-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1432-116">S_OK</span></span> 
  
> <span data-ttu-id="c1432-117">Таблица была успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="c1432-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="c1432-118">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="c1432-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c1432-119">Установлен флаг МАПИ_УНИКОДЕ, а сеанс не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="c1432-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1432-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1432-120">Remarks</span></span>

<span data-ttu-id="c1432-121">Метод **IMAPISession:: жетмсгсторестабле** извлекает указатель на таблицу хранилища сообщений, таблицу, поддерживаемую MAPI, которая содержит сведения о каждом открытом хранилище сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="c1432-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="c1432-122">Полный список обязательных и необязательных столбцов в таблице хранилища сообщений представлен в статье [Message Store Tables](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c1432-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c1432-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c1432-123">Notes to callers</span></span>

<span data-ttu-id="c1432-124">Так как MAPI обновляет таблицу хранилища сообщений во время сеанса, когда происходит изменение, вызовите метод **advise** таблицы хранилища сообщений, чтобы зарегистрировать уведомления об этих изменениях.</span><span class="sxs-lookup"><span data-stu-id="c1432-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="c1432-125">Возможные изменения включают добавление новых хранилищ сообщений, удаление существующих хранилищ и изменения в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1432-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="c1432-126">Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="c1432-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="c1432-127">Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="c1432-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1432-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c1432-128">MFCMAPI reference</span></span>

<span data-ttu-id="c1432-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c1432-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1432-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c1432-130">**File**</span></span>|<span data-ttu-id="c1432-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c1432-131">**Function**</span></span>|<span data-ttu-id="c1432-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c1432-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1432-133">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="c1432-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="c1432-134">Кмаиндлг:: Онопенмессажесторетабле</span><span class="sxs-lookup"><span data-stu-id="c1432-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="c1432-135">MFCMAPI использует метод **IMAPISession:: жетмсгсторестабле** , чтобы получить таблицу хранилища сообщений, чтобы ее можно было отобразить в главном диалоговом окне MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="c1432-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1432-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c1432-136">See also</span></span>



[<span data-ttu-id="c1432-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="c1432-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="c1432-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1432-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="c1432-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c1432-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="c1432-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c1432-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c1432-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c1432-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="c1432-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c1432-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="c1432-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="c1432-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="c1432-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1432-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="c1432-145">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="c1432-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c1432-146">Таблицы хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="c1432-146">Message Store Tables</span></span>](message-store-tables.md)

