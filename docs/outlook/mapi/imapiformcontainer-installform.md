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
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает форму в библиотеку форм.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом. Параметр _ulUIParam_ игнорируется, если клиентская MAPI_DIALOG в параметре _ulFlags._ Параметр  _ulUIParam_ может быть NULL, если MAPI_DIALOG также не пройден. 
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют установку формы. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно для предоставления сведений о ходе выполнения или запроса дополнительных сведений для пользователя. Если этот флаг не установлен, диалоговое окно не отображается.
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Если уже существует другая форма, которая обрабатывает класс сообщений, обрабатываемый этой формой, замените существующую форму на эту. Этот флаг игнорируется, если MAPI_DIALOG также присутствует. 
    
 _szCfgPathName_
  
> [in] Путь к файлу конфигурации формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Произошла ошибка реализации. Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, позвоните по методу [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md) 
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил установку формы, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики библиотек форм должны заполнять структуру **MAPIERROR** и возвращать MAPI_E_EXTENDED_ERROR, если возникают какие-либо из следующих условий: 
  
- Файл конфигурации не найден.
    
- Файл конфигурации не читается.
    
- Файл конфигурации недействителен.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения звонят **методу IMAPIFormContainer::InstallForm,** чтобы установить форму в определенный контейнер формы. Параметр  _szCfgPathName_ должен содержать путь файла конфигурации формы (то есть файла с расширением .cfg, описываемого формой и ее реализацией). Флаги в параметре  _ulFlags указывают_ следующее: 
  
- Если флаг MAPI_DIALOG, отображается пользовательский интерфейс, позволяющий пользователю, который устанавливает форму, указывать сведения об установке.
    
- Если флаг MAPIFORM_INSTALL_OVERWRITEONCONFLICT, любая предыдущая форма для того же класса сообщений заменяется установленной формой. В противном случае установка формы сливаются с текущим описанием формы, если оно существует.
    
- Если MAPI_DIALOG установлено, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.
    
- Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в наборе флагов означает, что будет сделано слияние. Все новые платформы в файле .cfg, которые в настоящее время не присутствуют в описании формы, будут установлены, и никаких других изменений не произойдет.
    
- Если флаг MAPI_UNICODE, путь файла конфигурации формы — строка Юникод. 
    
Клиенты должны вызвать [IMAPIFormContainer::GetLastError,](imapiformcontainer-getlasterror.md) если **InstallForm** возвращается MAPI_E_EXTENDED_ERROR, и они должны проверить возвращенную структуру [MAPIERROR,](mapierror.md) чтобы определить условие, которое подняло ошибку. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI использует **метод IMAPIFormContainer::InstallForm** для установки формы в контейнере формы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

