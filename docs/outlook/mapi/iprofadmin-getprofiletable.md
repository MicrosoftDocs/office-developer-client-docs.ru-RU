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
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809516"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="ee831-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="ee831-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="ee831-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee831-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee831-105">Предоставляет доступ к таблице профилей таблицу, содержащую сведения обо всех доступных профилей.</span><span class="sxs-lookup"><span data-stu-id="ee831-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ee831-106">���������</span><span class="sxs-lookup"><span data-stu-id="ee831-106">Parameters</span></span>

 <span data-ttu-id="ee831-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee831-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ee831-108">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ee831-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="ee831-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ee831-109">_lppTable_</span></span>
  
> <span data-ttu-id="ee831-110">[out] Указатель на указатель в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="ee831-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee831-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="ee831-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="ee831-112">S_OK</span></span> 
  
> <span data-ttu-id="ee831-113">В таблице профиль был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="ee831-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee831-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee831-114">Remarks</span></span>

<span data-ttu-id="ee831-115">Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профиля, который содержит одну строку для всех доступных профилей.</span><span class="sxs-lookup"><span data-stu-id="ee831-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="ee831-116">В каждой строке есть только два столбца: отображаемое имя профиля и флаг, указывающий, является ли профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee831-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="ee831-117">Профили, которые были удалены или используются, однако помечены для удаления, не включаются в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="ee831-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="ee831-118">В таблице профилей является статическим. последующие добавления и удаления профилей, не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="ee831-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="ee831-119">Если профили не существует, **GetProfileTable** возвращает таблицу с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="ee831-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="ee831-120">Дополнительные сведения о таблице профилей см [Профиля](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ee831-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ee831-121">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="ee831-121">MFCMAPI reference</span></span>

<span data-ttu-id="ee831-122">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="ee831-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ee831-123">**����**</span><span class="sxs-lookup"><span data-stu-id="ee831-123">**File**</span></span>|<span data-ttu-id="ee831-124">**�������**</span><span class="sxs-lookup"><span data-stu-id="ee831-124">**Function**</span></span>|<span data-ttu-id="ee831-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="ee831-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee831-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ee831-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ee831-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="ee831-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="ee831-128">Mfcmapi (en) использует метод **IProfAdmin::GetProfileTable** для получения профиля таблицу для отображения в диалоговом окне новый.</span><span class="sxs-lookup"><span data-stu-id="ee831-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee831-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ee831-129">See also</span></span>



[<span data-ttu-id="ee831-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee831-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="ee831-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ee831-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ee831-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee831-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="ee831-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ee831-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

