---
title: ипрофадминжетпрофилетабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414648"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="993cc-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="993cc-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="993cc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="993cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="993cc-105">Предоставляет доступ к таблице профилей — таблице, содержащей сведения обо всех доступных профилях.</span><span class="sxs-lookup"><span data-stu-id="993cc-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="993cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="993cc-106">Parameters</span></span>

 <span data-ttu-id="993cc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="993cc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="993cc-108">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="993cc-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="993cc-109">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="993cc-109">_lppTable_</span></span>
  
> <span data-ttu-id="993cc-110">вышли Указатель на указатель на таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="993cc-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="993cc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="993cc-111">Return value</span></span>

<span data-ttu-id="993cc-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="993cc-112">S_OK</span></span> 
  
> <span data-ttu-id="993cc-113">Таблица профилей успешно получена.</span><span class="sxs-lookup"><span data-stu-id="993cc-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="993cc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="993cc-114">Remarks</span></span>

<span data-ttu-id="993cc-115">Метод **ипрофадмин:: жетпрофилетабле** предоставляет доступ к таблице профилей, которая содержит одну строку для каждого доступного профиля.</span><span class="sxs-lookup"><span data-stu-id="993cc-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="993cc-116">В каждой строке имеется только два столбца: отображаемое имя профиля и флаг, указывающий, является ли профиль установленным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="993cc-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="993cc-117">Профили, которые были удалены или используются, но помечены для удаления, не включаются в таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="993cc-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="993cc-118">Таблица профилей является статической; последующие добавления и удаления профилей не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="993cc-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="993cc-119">Если профили не существуют, **жетпрофилетабле** возвращает таблицу с нулевыми строками.</span><span class="sxs-lookup"><span data-stu-id="993cc-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="993cc-120">Дополнительные сведения о таблице Profile содержатся в статье [Profile Tables](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="993cc-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="993cc-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="993cc-121">MFCMAPI reference</span></span>

<span data-ttu-id="993cc-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="993cc-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="993cc-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="993cc-123">**File**</span></span>|<span data-ttu-id="993cc-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="993cc-124">**Function**</span></span>|<span data-ttu-id="993cc-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="993cc-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="993cc-126">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="993cc-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="993cc-127">Кмаиндлг:: Оншовпрофилес</span><span class="sxs-lookup"><span data-stu-id="993cc-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="993cc-128">MFCMAPI использует метод **ипрофадмин:: жетпрофилетабле** , чтобы получить таблицу профилей, отображаемую в новом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="993cc-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="993cc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="993cc-129">See also</span></span>



[<span data-ttu-id="993cc-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="993cc-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="993cc-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="993cc-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="993cc-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="993cc-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="993cc-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="993cc-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

