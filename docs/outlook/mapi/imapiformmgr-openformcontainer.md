---
title: Имапиформмгропенформконтаинер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321639"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="69c28-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="69c28-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="69c28-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69c28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69c28-105">Открывает интерфейс [имапиформконтаинер](imapiformcontaineriunknown.md) для определенного контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="69c28-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="69c28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69c28-106">Parameters</span></span>

 <span data-ttu-id="69c28-107">_хфрмрег_</span><span class="sxs-lookup"><span data-stu-id="69c28-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="69c28-108">возврата Перечисление ХФРМРЕГ, которое указывает открываемую библиотеку форм (то есть, открываемый контейнер формы).</span><span class="sxs-lookup"><span data-stu-id="69c28-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="69c28-109">Перечисление ХФРМРЕГ — это перечисление, относящееся к поставщику библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="69c28-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="69c28-110">Возможные значения ХФРМРЕГ включают следующее:</span><span class="sxs-lookup"><span data-stu-id="69c28-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="69c28-111">ХФРМРЕГ_ДЕФАУЛТ</span><span class="sxs-lookup"><span data-stu-id="69c28-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="69c28-112">Удобный контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="69c28-112">A convenient form container.</span></span>
    
<span data-ttu-id="69c28-113">ХФРМРЕГ_ФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="69c28-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="69c28-114">Контейнер папок.</span><span class="sxs-lookup"><span data-stu-id="69c28-114">A folder container.</span></span> 
    
<span data-ttu-id="69c28-115">ХФРМРЕГ_ПЕРСОНАЛ</span><span class="sxs-lookup"><span data-stu-id="69c28-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="69c28-116">Контейнер для хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69c28-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="69c28-117">ХФРМРЕГ_ЛОКАЛ</span><span class="sxs-lookup"><span data-stu-id="69c28-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="69c28-118">Локальный контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="69c28-118">A local form container.</span></span> 
    
 <span data-ttu-id="69c28-119">_лпунк_</span><span class="sxs-lookup"><span data-stu-id="69c28-119">_lpunk_</span></span>
  
> <span data-ttu-id="69c28-120">возврата Указатель на объект, для которого открыт интерфейс.</span><span class="sxs-lookup"><span data-stu-id="69c28-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="69c28-121">Параметр _лпунк_ должен иметь **значение NULL** , если для параметра _хфрмрег_ не требуется указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="69c28-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="69c28-122">_лппфкнт_</span><span class="sxs-lookup"><span data-stu-id="69c28-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="69c28-123">вышли Указатель на указатель на возвращенный объект контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="69c28-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69c28-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69c28-124">Return value</span></span>

<span data-ttu-id="69c28-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="69c28-125">S_OK</span></span> 
  
> <span data-ttu-id="69c28-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="69c28-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="69c28-127">МАПИ_Е_НО_ИНТЕРФАЦЕ</span><span class="sxs-lookup"><span data-stu-id="69c28-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="69c28-128">Объект, на который указывает _лпунк_ , не поддерживает требуемый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="69c28-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="69c28-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="69c28-129">Remarks</span></span>

<span data-ttu-id="69c28-130">Средства просмотра форм вызывают метод **имапиформмгр:: опенформконтаинер** для открытия интерфейса **имапиформконтаинер** для определенного контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="69c28-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="69c28-131">Этот интерфейс затем можно использовать для установки форм и удаления форм из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="69c28-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="69c28-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="69c28-132">Notes to callers</span></span>

<span data-ttu-id="69c28-133">Если значение в _хфрмрег_ — хфрмрег_фолдер, идентификатор интерфейса, используемый в _лпунк_ , должен иметь значение, отличное от **null** , и разрешить вызов метода [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в интерфейс [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="69c28-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="69c28-134">Чтобы открыть локальный контейнер форм, необходимо использовать метод Call для **опенформконтаинер** или функцию [мапиопенлокалформконтаинер](mapiopenlocalformcontainer.md) ; невозможно использовать метод [имапиформмгр:: селектформконтаинер](imapiformmgr-selectformcontainer.md) , чтобы позволить пользователю выбрать локальный контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="69c28-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="69c28-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69c28-135">MFCMAPI reference</span></span>

<span data-ttu-id="69c28-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="69c28-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69c28-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="69c28-137">**File**</span></span>|<span data-ttu-id="69c28-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="69c28-138">**Function**</span></span>|<span data-ttu-id="69c28-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="69c28-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69c28-140">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="69c28-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="69c28-141">Кмаиндлг:: Онопенформконтаинер</span><span class="sxs-lookup"><span data-stu-id="69c28-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="69c28-142">MFCMAPI использует метод **имапиформмгр:: опенформконтаинер** для получения контейнера формы, чтобы можно было отобразить содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="69c28-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="69c28-143">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="69c28-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="69c28-144">Кмсгсторедлг:: Онопенформконтаинер</span><span class="sxs-lookup"><span data-stu-id="69c28-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="69c28-145">MFCMAPI использует метод **имапиформмгр:: опенформконтаинер** для получения контейнера формы для папки, чтобы можно было отобразить содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="69c28-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69c28-146">См. также</span><span class="sxs-lookup"><span data-stu-id="69c28-146">See also</span></span>



[<span data-ttu-id="69c28-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="69c28-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="69c28-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="69c28-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="69c28-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="69c28-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="69c28-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69c28-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="69c28-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="69c28-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

