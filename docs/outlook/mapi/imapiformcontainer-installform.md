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
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает формы в библиотеке форм.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод. Параметр _ulUIParam_ игнорируется, если клиентское приложение задает флаг MAPI_DIALOG с помощью параметра _ulFlags_ . Параметр _ulUIParam_ может иметь значение NULL, если не проходят MAPI_DIALOG. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет установкой формы. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно для предоставления сведений о ходе выполнения или запрашивать у пользователя для получения дополнительных сведений. Если этот флаг не установлен, диалоговое окно не отображается.
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Если другой формы уже существует, дескрипторы классом сообщения обрабатывается с помощью этой формы, замените существующей формы с этим сообщением. Этот флаг игнорируется, если также присутствует флаг MAPI_DIALOG. 
    
 _szCfgPathName_
  
> [in] Путь к файлу конфигурации формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_EXTENDED_ERROR 
  
> Произошла ошибка реализации. Чтобы получить структура [MAPIERROR](mapierror.md) , связанный с ошибкой, вызовите метод [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил установку формы, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="notes-to-implementers"></a>Примечания для реализующих

Поставщики библиотеки форм следует заполнить структуру **MAPIERROR** и возвращает MAPI_E_EXTENDED_ERROR при возникновении одного из следующих условий: 
  
- Файл конфигурации не найден.
    
- Файл конфигурации недоступен для чтения.
    
- Недопустимый файл конфигурации.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Клиентские приложения вызовите метод **IMAPIFormContainer::InstallForm** для установки формы в форме контейнер. Параметр _szCfgPathName_ должен содержать путь к файлу конфигурации формы (то есть, файл с расширением .cfg, описывающего формы и его реализация). Флаги в параметре _ulFlags_ укажите следующие параметры. 
  
- Если значение флага MAPI_DIALOG, отображается пользовательский интерфейс, позволяя пользователям, который выполняет установку форму, чтобы указать подробные сведения об установке.
    
- Если значение флага MAPIFORM_INSTALL_OVERWRITEONCONFLICT, любой предыдущей формы для того же класса сообщения заменяется формы установлен. В противном случае установки формы объединяются с описание текущей формы, если он существует.
    
- Если значение MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.
    
- Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в флаг задайте означает, что будет выполнено слияние. Новые платформы в файле .cfg, которые не представлены в настоящее время в описании формы будет установлен и нет других изменений внесено не будет.
    
- Если значение флага MAPI_UNICODE, путь к файлу конфигурации формы — это строка Юникод. 
    
Клиенты должны вызывать [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) , если **InstallForm** возвращает MAPI_E_EXTENDED_ERROR, и они должен проверить, возвращенные структура [MAPIERROR](mapierror.md) для определения состояния, которая вызвала ошибку. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |Mfcmapi (en) использует метод **IMAPIFormContainer::InstallForm** для установки формы в контейнере формы.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

