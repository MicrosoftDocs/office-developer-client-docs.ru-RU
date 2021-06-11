---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408553"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устраняет класс сообщения в его форму в контейнере формы и возвращает информационный объект формы для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameters

 _szMessageClass_
  
> [in] Строка, которая называет разрешенный класс сообщений. Имена классов сообщений всегда являются строками ANSI, а не Unicode.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют решение класса сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Разрешены только строки класса сообщений, которые соответствуют точному типу.
    
 _ppforminfo_
  
> [вышел] Указатель на указатель на возвращенный информационный объект формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщений, переданный в  _параметре szMessageClass,_ не соответствует классу сообщений для любой формы в контейнере формы. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения звонят по методу **IMAPIFormContainer::ResolveMessageClass,** чтобы разрешить класс сообщений в форму в контейнере формы. Объект информации формы, возвращаемый в  _параметре ppforminfo,_ предоставляет дополнительный доступ к свойствам формы с данным классом сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить класс сообщения в форму, передай имя разрешенного класса сообщений  `IPM.HelpDesk.Software` (например). Чтобы заставить разрешение быть точным (то есть для предотвращения разрешения для базового класса класса сообщений), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._ 
  
Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы. Не предполагайте, что идентификатор класса существует в библиотеке OLE до тех пор, пока не будет вызываться метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI использует **метод IMAPIFormContainer::ResolveMessageClass,** чтобы найти форму, связанную с классом сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

