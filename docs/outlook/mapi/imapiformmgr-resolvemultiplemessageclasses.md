---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571698"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Параметры

 _pMsgClasses_
  
> [in] Указатель на массив, содержащий имена классов сообщений для решения.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как разрешаются классов сообщений. Можно задать следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Следует разрешить только класс строки сообщения, которые являются точное совпадение.
    
MAPIFORM_LOCALONLY
  
> Не включайте кэшированные формы.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержащую форму, разрешения которого класс сообщения. Параметр _pFolderFocus_ может быть NULL. 
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на массив объектов данные формы. Если средство просмотра формы с помощью параметра _pMsgClasses_ передает значение NULL, параметр _ppfrminfoarray_ содержит объекты формы для всех форм в контейнере. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Средства просмотра форм вызовите метод **IMAPIFormMgr::ResolveMultipleMessageClasses** для разрешения группы классов сообщений для форм в контейнере формы. Массив объектов формы сведений, возвращаемых _ppfrminfoarray_ дальнейшей предоставляет доступ к каждой из свойства форм. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для разрешения группы классов сообщений в формах, форма просмотра передает в массиве разрешения имен классов сообщений. Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класс сообщения, когда точно соответствующие формы сервер не доступен) флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ . 
  
Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.
  
Если класс сообщения не может быть разрешен в форму, для этого класса сообщений в массиве сведения формы будет возвращено значение NULL. Таким образом даже в том случае, если метод возвращает значение S_OK, средства просмотра формы не должны работать предполагается, что все классы сообщений устранены успешно. Вместо этого средства просмотра формы должен проверить, значения в массиве.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

