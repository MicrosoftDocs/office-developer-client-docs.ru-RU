---
title: IProfAdminGetProfileTable
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
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="d99c2-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="d99c2-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="d99c2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d99c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d99c2-105">Предоставляет доступ к таблице профилей, таблице, содержаной сведения обо всех доступных профилях.</span><span class="sxs-lookup"><span data-stu-id="d99c2-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d99c2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d99c2-106">Parameters</span></span>

 <span data-ttu-id="d99c2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d99c2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d99c2-108">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="d99c2-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="d99c2-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d99c2-109">_lppTable_</span></span>
  
> <span data-ttu-id="d99c2-110">[вышел] Указатель на указатель на таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="d99c2-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d99c2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d99c2-111">Return value</span></span>

<span data-ttu-id="d99c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d99c2-112">S_OK</span></span> 
  
> <span data-ttu-id="d99c2-113">Таблица профилей была успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="d99c2-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d99c2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d99c2-114">Remarks</span></span>

<span data-ttu-id="d99c2-115">Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профилей, которая содержит одну строку для каждого доступного профиля.</span><span class="sxs-lookup"><span data-stu-id="d99c2-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="d99c2-116">В каждой строке есть только два столбца: имя отображения профиля и флаг, который указывает, является ли профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d99c2-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="d99c2-117">Профили, которые были удалены или используются, но помечены для удаления, не включаются в таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="d99c2-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="d99c2-118">Таблица профилей статична; последующие добавления и удаления профилей не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="d99c2-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="d99c2-119">Если профили не существуют, **GetProfileTable** возвращает таблицу с нулевыми строками.</span><span class="sxs-lookup"><span data-stu-id="d99c2-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="d99c2-120">Дополнительные сведения о таблице профилей см. в таблице ["Таблицы профилей".](profile-tables.md)</span><span class="sxs-lookup"><span data-stu-id="d99c2-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d99c2-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d99c2-121">MFCMAPI reference</span></span>

<span data-ttu-id="d99c2-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d99c2-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d99c2-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d99c2-123">**File**</span></span>|<span data-ttu-id="d99c2-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d99c2-124">**Function**</span></span>|<span data-ttu-id="d99c2-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d99c2-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d99c2-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d99c2-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="d99c2-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="d99c2-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="d99c2-128">MFCMAPI использует **метод IProfAdmin::GetProfileTable** для отображения таблицы профилей в новом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d99c2-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d99c2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d99c2-129">See also</span></span>



[<span data-ttu-id="d99c2-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d99c2-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d99c2-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="d99c2-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="d99c2-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d99c2-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="d99c2-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d99c2-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

