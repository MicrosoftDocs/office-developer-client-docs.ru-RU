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
ms.openlocfilehash: fd7bc8f051e9584fc63f22bdbaf9696c2e4d15a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580938"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="6fdae-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="6fdae-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="6fdae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fdae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fdae-105">Устанавливает формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="6fdae-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="6fdae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fdae-106">Parameters</span></span>

 <span data-ttu-id="6fdae-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6fdae-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6fdae-108">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="6fdae-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="6fdae-109">Параметр _ulUIParam_ игнорируется, если клиентское приложение задает флаг MAPI_DIALOG с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6fdae-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6fdae-110">Параметр _ulUIParam_ может иметь значение NULL, если не проходят MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="6fdae-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="6fdae-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fdae-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6fdae-112">[in] Битовая маска флаги, который управляет установкой формы.</span><span class="sxs-lookup"><span data-stu-id="6fdae-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="6fdae-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="6fdae-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6fdae-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6fdae-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6fdae-115">Отображает диалоговое окно для предоставления сведений о ходе выполнения или запрашивать у пользователя для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="6fdae-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="6fdae-116">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="6fdae-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="6fdae-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6fdae-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6fdae-118">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="6fdae-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6fdae-119">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6fdae-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="6fdae-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="6fdae-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="6fdae-121">Если другой формы уже существует, дескрипторы классом сообщения обрабатывается с помощью этой формы, замените существующей формы с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="6fdae-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="6fdae-122">Этот флаг игнорируется, если также присутствует флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="6fdae-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="6fdae-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="6fdae-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="6fdae-124">[in] Путь к файлу конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="6fdae-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fdae-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fdae-125">Return value</span></span>

<span data-ttu-id="6fdae-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fdae-126">S_OK</span></span> 
  
> <span data-ttu-id="6fdae-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6fdae-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6fdae-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="6fdae-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="6fdae-129">Произошла ошибка реализации.</span><span class="sxs-lookup"><span data-stu-id="6fdae-129">An implementation error occurred.</span></span> <span data-ttu-id="6fdae-130">Чтобы получить структура [MAPIERROR](mapierror.md) , связанный с ошибкой, вызовите метод [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdae-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="6fdae-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6fdae-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6fdae-132">Пользователь отменил установку формы, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6fdae-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="6fdae-133">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="6fdae-133">Notes to implementers</span></span>

<span data-ttu-id="6fdae-134">Поставщики библиотеки форм следует заполнить структуру **MAPIERROR** и возвращает MAPI_E_EXTENDED_ERROR при возникновении одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="6fdae-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="6fdae-135">Файл конфигурации не найден.</span><span class="sxs-lookup"><span data-stu-id="6fdae-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="6fdae-136">Файл конфигурации недоступен для чтения.</span><span class="sxs-lookup"><span data-stu-id="6fdae-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="6fdae-137">Недопустимый файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6fdae-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="6fdae-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6fdae-138">Notes to callers</span></span>

<span data-ttu-id="6fdae-139">Клиентские приложения вызовите метод **IMAPIFormContainer::InstallForm** для установки формы в форме контейнер.</span><span class="sxs-lookup"><span data-stu-id="6fdae-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="6fdae-140">Параметр _szCfgPathName_ должен содержать путь к файлу конфигурации формы (то есть, файл с расширением .cfg, описывающего формы и его реализация).</span><span class="sxs-lookup"><span data-stu-id="6fdae-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="6fdae-141">Флаги в параметре _ulFlags_ укажите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6fdae-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="6fdae-142">Если значение флага MAPI_DIALOG, отображается пользовательский интерфейс, позволяя пользователям, который выполняет установку форму, чтобы указать подробные сведения об установке.</span><span class="sxs-lookup"><span data-stu-id="6fdae-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="6fdae-143">Если значение флага MAPIFORM_INSTALL_OVERWRITEONCONFLICT, любой предыдущей формы для того же класса сообщения заменяется формы установлен.</span><span class="sxs-lookup"><span data-stu-id="6fdae-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="6fdae-144">В противном случае установки формы объединяются с описание текущей формы, если он существует.</span><span class="sxs-lookup"><span data-stu-id="6fdae-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="6fdae-145">Если значение MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fdae-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="6fdae-146">Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в флаг задайте означает, что будет выполнено слияние.</span><span class="sxs-lookup"><span data-stu-id="6fdae-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="6fdae-147">Новые платформы в файле .cfg, которые не представлены в настоящее время в описании формы будет установлен и нет других изменений внесено не будет.</span><span class="sxs-lookup"><span data-stu-id="6fdae-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="6fdae-148">Если значение флага MAPI_UNICODE, путь к файлу конфигурации формы — это строка Юникод.</span><span class="sxs-lookup"><span data-stu-id="6fdae-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="6fdae-149">Клиенты должны вызывать [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) , если **InstallForm** возвращает MAPI_E_EXTENDED_ERROR, и они должен проверить, возвращенные структура [MAPIERROR](mapierror.md) для определения состояния, которая вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="6fdae-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fdae-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6fdae-150">MFCMAPI reference</span></span>

<span data-ttu-id="6fdae-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6fdae-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fdae-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6fdae-152">**File**</span></span>|<span data-ttu-id="6fdae-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6fdae-153">**Function**</span></span>|<span data-ttu-id="6fdae-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6fdae-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fdae-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6fdae-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6fdae-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="6fdae-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="6fdae-157">Mfcmapi (en) использует метод **IMAPIFormContainer::InstallForm** для установки формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="6fdae-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fdae-158">См. также</span><span class="sxs-lookup"><span data-stu-id="6fdae-158">See also</span></span>



[<span data-ttu-id="6fdae-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6fdae-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6fdae-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fdae-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6fdae-161">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6fdae-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

