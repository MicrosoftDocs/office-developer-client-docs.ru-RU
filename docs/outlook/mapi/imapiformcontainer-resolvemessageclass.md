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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешит класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Параметры

 _szMessageClass_
  
> [in] Строка, которая именует класс сообщения, который будет разрешен. Имена классов сообщений всегда являются строками ANSI, а не Юникодом.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет решением класса сообщения. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Должны быть разрешены только строки класса сообщений, точно совпадают.
    
 _ppforminfo_
  
> [out] Указатель на указатель на возвращенный объект сведений формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданный в  _параметре szMessageClass,_ не соответствует классу сообщения для любой формы в контейнере формы. 
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывать метод **IMAPIFormContainer::ResolveMessageClass,** чтобы разрешить класс сообщения в форму в контейнере формы. Объект сведений о форме, возвращенный в  _параметре ppforminfo,_ предоставляет дополнительный доступ к свойствам формы с данным классом сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить класс сообщения в форму, передав имя класса сообщения, который необходимо разрешить (например,  `IPM.HelpDesk.Software` ). Чтобы разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._ 
  
Идентификатор класса разрешенного сообщения возвращается как часть объекта сведений формы. Не предполагайте, что идентификатор класса существует в библиотеке OLE до вызова метода [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI использует метод **IMAPIFormContainer::ResolveMessageClass** для поиска формы, связанной с классом сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

