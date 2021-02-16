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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устанавливает форму в библиотеку форм.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays. Параметр _ulUIParam_ игнорируется, если клиентские приложения не MAPI_DIALOG флага в _параметре ulFlags._ Параметр  _ulUIParam_ может иметь NULL, MAPI_DIALOG также не передается. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет установкой формы. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно для предоставления сведений о ходе выполнения или запроса дополнительных сведений. Если этот флаг не установлен, диалоговое окно не отображается.
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Если уже существует другая форма, которая обрабатывает класс сообщения, обрабатываемого этой формой, замените существующую форму на эту. Этот флаг игнорируется, если MAPI_DIALOG также присутствует. 
    
 _szCfgPathName_
  
> [in] Путь к файлу конфигурации формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Произошла ошибка реализации. Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, вызовите метод [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md) 
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил установку формы, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики библиотек форм должны заполнить структуру **MAPIERROR** и возвращать MAPI_E_EXTENDED_ERROR при любом из следующих условий: 
  
- Файл конфигурации не найден.
    
- Файл конфигурации нечитаемый.
    
- Недопустимый файл конфигурации.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения вызывать метод **IMAPIFormContainer::InstallForm,** чтобы установить форму в определенный контейнер формы. Параметр  _szCfgPathName_ должен содержать путь к файлу конфигурации формы (то есть файлу с расширением CFG, описывая форму и ее реализацию). Флаги в параметре  _ulFlags_ указывают следующее: 
  
- Если установлен MAPI_DIALOG, отображается пользовательский интерфейс, позволяющий пользователю, устанавливая форму, указывать сведения об установке.
    
- Если установлен MAPIFORM_INSTALL_OVERWRITEONCONFLICT, любая предыдущая форма для того же класса сообщения заменяется устанавливаемой формой. В противном случае установка формы будет объединена с текущим описанием формы, если оно существует.
    
- Если MAPI_DIALOG установлен, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.
    
- Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в наборе флагов означает, что будет сделано слияние. Все новые платформы в файле CFG, которые в настоящее время не присутствуют в описании формы, будут установлены, и никакие другие изменения не будут внесены.
    
- Если установлен MAPI_UNICODE, путь к файлу конфигурации формы является строкой Юникода. 
    
Клиенты должны вызывать [IMAPIFormContainer::GetLastError,](imapiformcontainer-getlasterror.md) если **InstallForm** возвращает MAPI_E_EXTENDED_ERROR, и им следует проверить возвращенную структуру [MAPIERROR,](mapierror.md) чтобы определить условие, которое вызывало ошибку. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI использует метод **IMAPIFormContainer::InstallForm** для установки формы в контейнере формы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

