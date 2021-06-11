---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405088"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="6603a-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="6603a-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="6603a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6603a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6603a-105">Устанавливает форму в библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="6603a-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="6603a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6603a-106">Parameters</span></span>

 <span data-ttu-id="6603a-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6603a-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6603a-108">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="6603a-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="6603a-109">Параметр _ulUIParam_ игнорируется, если клиентская MAPI_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6603a-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6603a-110">Параметр  _ulUIParam_ может быть NULL, если MAPI_DIALOG также не пройден.</span><span class="sxs-lookup"><span data-stu-id="6603a-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="6603a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6603a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6603a-112">[in] Битмашка флагов, которые контролируют установку формы.</span><span class="sxs-lookup"><span data-stu-id="6603a-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="6603a-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6603a-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6603a-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6603a-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6603a-115">Отображает диалоговое окно для предоставления сведений о ходе выполнения или запроса дополнительных сведений для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6603a-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="6603a-116">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="6603a-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="6603a-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6603a-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6603a-118">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="6603a-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6603a-119">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6603a-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="6603a-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="6603a-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="6603a-121">Если уже существует другая форма, которая обрабатывает класс сообщений, обрабатываемый этой формой, замените существующую форму на эту.</span><span class="sxs-lookup"><span data-stu-id="6603a-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="6603a-122">Этот флаг игнорируется, если MAPI_DIALOG также присутствует.</span><span class="sxs-lookup"><span data-stu-id="6603a-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="6603a-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="6603a-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="6603a-124">[in] Путь к файлу конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="6603a-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6603a-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6603a-125">Return value</span></span>

<span data-ttu-id="6603a-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="6603a-126">S_OK</span></span> 
  
> <span data-ttu-id="6603a-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6603a-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6603a-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="6603a-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="6603a-129">Произошла ошибка реализации.</span><span class="sxs-lookup"><span data-stu-id="6603a-129">An implementation error occurred.</span></span> <span data-ttu-id="6603a-130">Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, позвоните по методу [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="6603a-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="6603a-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6603a-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6603a-132">Пользователь отменил установку формы, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6603a-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="6603a-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6603a-133">Notes to implementers</span></span>

<span data-ttu-id="6603a-134">Поставщики библиотек форм должны заполнять структуру **MAPIERROR** и возвращать MAPI_E_EXTENDED_ERROR, если возникают какие-либо из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="6603a-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="6603a-135">Файл конфигурации не найден.</span><span class="sxs-lookup"><span data-stu-id="6603a-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="6603a-136">Файл конфигурации не читается.</span><span class="sxs-lookup"><span data-stu-id="6603a-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="6603a-137">Файл конфигурации недействителен.</span><span class="sxs-lookup"><span data-stu-id="6603a-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="6603a-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6603a-138">Notes to callers</span></span>

<span data-ttu-id="6603a-139">Клиентские приложения звонят **методу IMAPIFormContainer::InstallForm,** чтобы установить форму в определенный контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="6603a-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="6603a-140">Параметр  _szCfgPathName_ должен содержать путь файла конфигурации формы (то есть файла с расширением .cfg, описываемого формой и ее реализацией).</span><span class="sxs-lookup"><span data-stu-id="6603a-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="6603a-141">Флаги в параметре  _ulFlags указывают_ следующее:</span><span class="sxs-lookup"><span data-stu-id="6603a-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="6603a-142">Если флаг MAPI_DIALOG, отображается пользовательский интерфейс, позволяющий пользователю, который устанавливает форму, указывать сведения об установке.</span><span class="sxs-lookup"><span data-stu-id="6603a-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="6603a-143">Если флаг MAPIFORM_INSTALL_OVERWRITEONCONFLICT, любая предыдущая форма для того же класса сообщений заменяется установленной формой.</span><span class="sxs-lookup"><span data-stu-id="6603a-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="6603a-144">В противном случае установка формы сливаются с текущим описанием формы, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="6603a-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="6603a-145">Если MAPI_DIALOG установлено, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6603a-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="6603a-146">Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в наборе флагов означает, что будет сделано слияние.</span><span class="sxs-lookup"><span data-stu-id="6603a-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="6603a-147">Все новые платформы в файле .cfg, которые в настоящее время не присутствуют в описании формы, будут установлены, и никаких других изменений не произойдет.</span><span class="sxs-lookup"><span data-stu-id="6603a-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="6603a-148">Если флаг MAPI_UNICODE, путь файла конфигурации формы — строка Юникод.</span><span class="sxs-lookup"><span data-stu-id="6603a-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="6603a-149">Клиенты должны вызвать [IMAPIFormContainer::GetLastError,](imapiformcontainer-getlasterror.md) если **InstallForm** возвращается MAPI_E_EXTENDED_ERROR, и они должны проверить возвращенную структуру [MAPIERROR,](mapierror.md) чтобы определить условие, которое подняло ошибку.</span><span class="sxs-lookup"><span data-stu-id="6603a-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6603a-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6603a-150">MFCMAPI reference</span></span>

<span data-ttu-id="6603a-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6603a-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6603a-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6603a-152">**File**</span></span>|<span data-ttu-id="6603a-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6603a-153">**Function**</span></span>|<span data-ttu-id="6603a-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6603a-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6603a-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6603a-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6603a-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="6603a-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="6603a-157">MFCMAPI использует **метод IMAPIFormContainer::InstallForm** для установки формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="6603a-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6603a-158">См. также</span><span class="sxs-lookup"><span data-stu-id="6603a-158">See also</span></span>



[<span data-ttu-id="6603a-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6603a-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6603a-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6603a-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6603a-161">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6603a-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

