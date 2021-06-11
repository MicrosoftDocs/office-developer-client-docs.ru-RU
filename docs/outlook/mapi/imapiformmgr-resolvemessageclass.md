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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устраняет класс сообщений в его форму в контейнере форм и возвращает информационный объект формы для этой формы.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Parameters

 _szMsgClass_
  
> [in] Строка, которая называет разрешенный класс сообщений.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют решение класса сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Разрешены только строки класса сообщений, которые соответствуют точному типу.
    
 _pFolderFocus_
  
> [in] Указатель на папку с разрешенным сообщением. Параметр  _pFolderFocus_ может быть NULL. 
    
 _ppResult_
  
> [вышел] Указатель на указатель на возвращенный информационный объект формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщений, переданный в  _параметре szMsgClass,_ не соответствует классу сообщений для любой формы в библиотеке форм. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr::ResolveMessageClass,** чтобы разрешить класс сообщений в его форме в контейнере формы. Объект информации о форме, возвращенный в  _параметре ppResult,_ предоставляет дополнительный доступ к свойствам формы, которая имеет данный класс сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить класс сообщений в форму, зритель формы передает имя разрешенного класса сообщений, например `IPM.HelpDesk.Software` "". Чтобы заставить разрешение быть точным (то есть предотвратить разрешение базового класса класса сообщений, когда не доступен точно совпадающий сервер формы), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._ Если  _параметром pFolderFocus_ является NULL, процесс разрешения класса сообщения не будет искать контейнер папки. 
  
Порядок поиска контейнеров зависит от реализации поставщика библиотеки форм. Поставщик библиотеки форм по умолчанию сначала выполняет поиск локального контейнера, затем контейнера папок для переданной папки, контейнера личной формы и, наконец, контейнера организации.
  
Имена классов сообщений всегда являются строками ANSI, а не Unicode.
  
Идентификатор класса для разрешенного класса сообщений возвращается как часть информационного объекта формы. Просмотр формы не должен работать с предположением о том, что идентификатор класса существует в библиотеке OLE до тех пор, пока зритель формы не вызвал метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) или [метод IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

