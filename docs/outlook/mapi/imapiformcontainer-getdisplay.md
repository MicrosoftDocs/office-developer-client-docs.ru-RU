---
title: Имапиформконтаинержетдисплай
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329430"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="ed192-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="ed192-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="ed192-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed192-105">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="ed192-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="ed192-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed192-106">Parameters</span></span>

 <span data-ttu-id="ed192-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed192-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ed192-108">возврата Битовая маска флагов, определяющая тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="ed192-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="ed192-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ed192-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ed192-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed192-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ed192-111">Возвращаемая строка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ed192-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="ed192-112">Если флаг МАПИ_УНИКОДЕ не установлен, строка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="ed192-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="ed192-113">_Псздисплайнаме_</span><span class="sxs-lookup"><span data-stu-id="ed192-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="ed192-114">вышли Указатель на строку, которая содержит отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="ed192-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed192-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed192-115">Return value</span></span>

<span data-ttu-id="ed192-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed192-116">S_OK</span></span> 
  
> <span data-ttu-id="ed192-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ed192-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ed192-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ed192-118">MFCMAPI reference</span></span>

<span data-ttu-id="ed192-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ed192-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ed192-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ed192-120">**File**</span></span>|<span data-ttu-id="ed192-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ed192-121">**Function**</span></span>|<span data-ttu-id="ed192-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ed192-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ed192-123">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="ed192-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="ed192-124">Кформконтаинердлг:: Кформконтаинердлг</span><span class="sxs-lookup"><span data-stu-id="ed192-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="ed192-125">MFCMAPI использует метод **имапиформконтаинер::** для получения имени контейнера формы при отображении кформконтаинердлг.</span><span class="sxs-lookup"><span data-stu-id="ed192-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed192-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ed192-126">See also</span></span>



[<span data-ttu-id="ed192-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed192-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="ed192-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ed192-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

