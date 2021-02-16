---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426396"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешит класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Параметры

 _szMsgClass_
  
> [in] Строка, которая именует класс сообщения, который будет разрешен.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет решением класса сообщения. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Должны быть разрешены только строки класса сообщений, точно совпадают.
    
 _pFolderFocus_
  
> [in] Указатель на папку, в которую входит разрешенное сообщение. Параметр  _pFolderFocus может_ иметь NULL. 
    
 _ppResult_
  
> [out] Указатель на указатель на возвращенный объект сведений о форме.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданный в  _параметре szMsgClass,_ не соответствует классу сообщения для любой формы в библиотеке форм. 
    
## <a name="remarks"></a>Примечания

С помощью метода **IMAPIFormMgr::ResolveMessageClass можно вызвать метод IMAPIFormMgr::ResolveMessageClass,** чтобы разрешить класс сообщения в форму в контейнере формы. Объект сведений о форме, возвращенный в  _параметре ppResult,_ предоставляет дополнительный доступ к свойствам формы, которая имеет заданный класс сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить класс сообщения в форму, просмотр формы передает имя разрешаемого класса сообщения, например `IPM.HelpDesk.Software` " ". Чтобы принудительное разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщений, когда сервер формы, точно совпадающий с другим, недо доступен), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._ Если параметр  _pFolderFocus_ имеет NULL, процесс разрешения класса сообщений не будет искать контейнер папок. 
  
Порядок ищите контейнеров зависит от реализации поставщика библиотеки форм. Поставщик библиотеки форм по умолчанию сначала выполняет поиск локального контейнера, а затем контейнера папки для переданной папки, контейнера личной формы и, наконец, контейнера организации.
  
Имена классов сообщений всегда являются строками ANSI, но не Юникодом.
  
Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы. Просмотр формы не должен работать при предположении, что идентификатор класса существует в библиотеке OLE, пока оно не будет вызвано [методом IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

