---
title: Имапиформконтаинерремовеформ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355747"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="9fc46-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="9fc46-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="9fc46-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fc46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fc46-105">Удаляет определенную форму из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="9fc46-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="9fc46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fc46-106">Parameters</span></span>

 <span data-ttu-id="9fc46-107">_Сзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="9fc46-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="9fc46-108">возврата Строка, которая называет класс сообщения формы, удаляемой из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="9fc46-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="9fc46-109">Имена классов сообщений всегда являются строками ANSI, а не Юникодом.</span><span class="sxs-lookup"><span data-stu-id="9fc46-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fc46-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fc46-110">Return value</span></span>

<span data-ttu-id="9fc46-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fc46-111">S_OK</span></span> 
  
> <span data-ttu-id="9fc46-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9fc46-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9fc46-113">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="9fc46-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9fc46-114">Класс сообщения, переданный в параметре _сзмессажекласс_ , не соответствует классу сообщения любой формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="9fc46-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9fc46-115">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9fc46-115">MFCMAPI reference</span></span>

<span data-ttu-id="9fc46-116">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9fc46-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9fc46-117">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9fc46-117">**File**</span></span>|<span data-ttu-id="9fc46-118">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9fc46-118">**Function**</span></span>|<span data-ttu-id="9fc46-119">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9fc46-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fc46-120">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="9fc46-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="9fc46-121">Кформконтаинердлг:: Онделетеселектедитем</span><span class="sxs-lookup"><span data-stu-id="9fc46-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9fc46-122">MFCMAPI использует метод **имапиформконтаинер:: ремовеформ** для удаления формы из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="9fc46-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fc46-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9fc46-123">See also</span></span>



[<span data-ttu-id="9fc46-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fc46-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="9fc46-125">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9fc46-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

