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
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588246"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="c1d80-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="c1d80-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="c1d80-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1d80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1d80-105">Предоставляет доступ к таблице профилей таблицу, содержащую сведения обо всех доступных профилей.</span><span class="sxs-lookup"><span data-stu-id="c1d80-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c1d80-106">���������</span><span class="sxs-lookup"><span data-stu-id="c1d80-106">Parameters</span></span>

 <span data-ttu-id="c1d80-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1d80-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c1d80-108">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c1d80-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="c1d80-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c1d80-109">_lppTable_</span></span>
  
> <span data-ttu-id="c1d80-110">[out] Указатель на указатель в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="c1d80-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1d80-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1d80-111">Return value</span></span>

<span data-ttu-id="c1d80-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1d80-112">S_OK</span></span> 
  
> <span data-ttu-id="c1d80-113">В таблице профиль был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="c1d80-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1d80-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c1d80-114">Remarks</span></span>

<span data-ttu-id="c1d80-115">Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профиля, который содержит одну строку для всех доступных профилей.</span><span class="sxs-lookup"><span data-stu-id="c1d80-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="c1d80-116">В каждой строке есть только два столбца: отображаемое имя профиля и флаг, указывающий, является ли профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1d80-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="c1d80-117">Профили, которые были удалены или используются, однако помечены для удаления, не включаются в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="c1d80-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="c1d80-118">В таблице профилей является статическим. последующие добавления и удаления профилей, не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="c1d80-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="c1d80-119">Если профили не существует, **GetProfileTable** возвращает таблицу с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="c1d80-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="c1d80-120">Дополнительные сведения о таблице профилей см [Профиля](profile-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c1d80-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1d80-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c1d80-121">MFCMAPI reference</span></span>

<span data-ttu-id="c1d80-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c1d80-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1d80-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c1d80-123">**File**</span></span>|<span data-ttu-id="c1d80-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c1d80-124">**Function**</span></span>|<span data-ttu-id="c1d80-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c1d80-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1d80-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c1d80-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="c1d80-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="c1d80-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="c1d80-128">Mfcmapi (en) использует метод **IProfAdmin::GetProfileTable** для получения профиля таблицу для отображения в диалоговом окне новый.</span><span class="sxs-lookup"><span data-stu-id="c1d80-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1d80-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c1d80-129">See also</span></span>



[<span data-ttu-id="c1d80-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1d80-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="c1d80-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="c1d80-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="c1d80-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1d80-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="c1d80-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c1d80-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

