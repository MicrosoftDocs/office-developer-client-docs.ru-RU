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
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="cefab-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="cefab-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="cefab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cefab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cefab-105">Предоставляет доступ к таблице профилей, которая содержит сведения обо всех доступных профилях.</span><span class="sxs-lookup"><span data-stu-id="cefab-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="cefab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cefab-106">Parameters</span></span>

 <span data-ttu-id="cefab-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cefab-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cefab-108">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="cefab-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="cefab-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="cefab-109">_lppTable_</span></span>
  
> <span data-ttu-id="cefab-110">[out] Указатель на указатель на таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="cefab-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cefab-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cefab-111">Return value</span></span>

<span data-ttu-id="cefab-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cefab-112">S_OK</span></span> 
  
> <span data-ttu-id="cefab-113">Таблица профилей успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="cefab-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cefab-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cefab-114">Remarks</span></span>

<span data-ttu-id="cefab-115">Метод **IProfAdmin::GetProfileTable** предоставляет доступ к таблице профилей, которая содержит одну строку для каждого доступного профиля.</span><span class="sxs-lookup"><span data-stu-id="cefab-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="cefab-116">В каждой строке есть только два столбца: отображаемая имя профиля и флаг, который указывает, является ли профиль профилем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cefab-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="cefab-117">Профили, которые были удалены или используются, но помечены для удаления, не включаются в таблицу профилей.</span><span class="sxs-lookup"><span data-stu-id="cefab-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="cefab-118">Таблица профилей является статической; последующие добавления и удаления профилей не отражаются в таблице.</span><span class="sxs-lookup"><span data-stu-id="cefab-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="cefab-119">Если профили не существуют, **GetProfileTable** возвращает таблицу с нулем строк.</span><span class="sxs-lookup"><span data-stu-id="cefab-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="cefab-120">Дополнительные сведения о таблице профилей см. в [таблицах профилей.](profile-tables.md)</span><span class="sxs-lookup"><span data-stu-id="cefab-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cefab-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cefab-121">MFCMAPI reference</span></span>

<span data-ttu-id="cefab-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="cefab-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cefab-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="cefab-123">**File**</span></span>|<span data-ttu-id="cefab-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="cefab-124">**Function**</span></span>|<span data-ttu-id="cefab-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="cefab-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cefab-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cefab-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="cefab-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="cefab-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="cefab-128">MFCMAPI использует метод **IProfAdmin::GetProfileTable** для отображения таблицы профилей в новом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cefab-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cefab-129">См. также</span><span class="sxs-lookup"><span data-stu-id="cefab-129">See also</span></span>



[<span data-ttu-id="cefab-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cefab-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="cefab-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="cefab-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="cefab-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cefab-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="cefab-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="cefab-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

