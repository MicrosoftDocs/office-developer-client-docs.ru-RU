---
title: IMAPISessionGetMsgStoresTable
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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809053"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="43ad4-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="43ad4-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="43ad4-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43ad4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43ad4-105">Предоставляет доступ к таблице хранилища сообщений, который содержит сведения о всех хранилищ сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="43ad4-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="43ad4-106">���������</span><span class="sxs-lookup"><span data-stu-id="43ad4-106">Parameters</span></span>

 <span data-ttu-id="43ad4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43ad4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="43ad4-108">[in] Битовая маска флаги, который определяет формат для столбцов, которые являются строками символов.</span><span class="sxs-lookup"><span data-stu-id="43ad4-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="43ad4-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="43ad4-109">The following flag can be set:</span></span>
    
<span data-ttu-id="43ad4-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43ad4-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="43ad4-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="43ad4-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="43ad4-112">Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="43ad4-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="43ad4-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="43ad4-113">_lppTable_</span></span>
  
> <span data-ttu-id="43ad4-114">[out] Указатель на указатель в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="43ad4-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43ad4-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="43ad4-115">Return value</span></span>

<span data-ttu-id="43ad4-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="43ad4-116">S_OK</span></span> 
  
> <span data-ttu-id="43ad4-117">Таблица успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="43ad4-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="43ad4-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="43ad4-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="43ad4-119">Был установлен флажок MAPI_UNICODE и сеанса не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="43ad4-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43ad4-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="43ad4-120">Remarks</span></span>

<span data-ttu-id="43ad4-121">Метод **IMAPISession::GetMsgStoresTable** получает указатель в таблице хранилища сообщений, таблицы задаваемые с помощью интерфейса MAPI, содержащий сведения о каждом открыть сообщение хранилище в профиле.</span><span class="sxs-lookup"><span data-stu-id="43ad4-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="43ad4-122">Полный список обязательные и дополнительные столбцы в сообщении хранилища в таблице, просматривать [Таблицы хранения сообщений](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="43ad4-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="43ad4-123">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="43ad4-123">Notes to callers</span></span>

<span data-ttu-id="43ad4-124">Так как MAPI обновляет таблицу хранилища сообщений во время сеанса при каждом возникновении изменений, вызовите метод **уведомлений** таблицы хранилища сообщений для регистрации уведомлений об этих изменений.</span><span class="sxs-lookup"><span data-stu-id="43ad4-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="43ad4-125">Возможные изменения включают добавление новых хранилищ сообщений, удаления существующих хранит и изменяется на хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43ad4-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="43ad4-126">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="43ad4-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="43ad4-127">Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="43ad4-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43ad4-128">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="43ad4-128">MFCMAPI reference</span></span>

<span data-ttu-id="43ad4-129">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="43ad4-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43ad4-130">**����**</span><span class="sxs-lookup"><span data-stu-id="43ad4-130">**File**</span></span>|<span data-ttu-id="43ad4-131">**�������**</span><span class="sxs-lookup"><span data-stu-id="43ad4-131">**Function**</span></span>|<span data-ttu-id="43ad4-132">**�����������**</span><span class="sxs-lookup"><span data-stu-id="43ad4-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43ad4-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="43ad4-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="43ad4-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="43ad4-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="43ad4-135">Mfcmapi (en) использует метод **IMAPISession::GetMsgStoresTable** для получения таблицы хранилища сообщений, чтобы он отображался в диалоговом окне основной mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="43ad4-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43ad4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="43ad4-136">See also</span></span>



[<span data-ttu-id="43ad4-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="43ad4-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="43ad4-138">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="43ad4-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="43ad4-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="43ad4-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="43ad4-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="43ad4-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="43ad4-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="43ad4-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="43ad4-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="43ad4-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="43ad4-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="43ad4-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="43ad4-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="43ad4-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="43ad4-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="43ad4-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="43ad4-146">Хранение сообщений таблиц</span><span class="sxs-lookup"><span data-stu-id="43ad4-146">Message Store Tables</span></span>](message-store-tables.md)

