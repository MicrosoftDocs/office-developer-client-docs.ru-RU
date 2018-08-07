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
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808964"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Относится к**: Outlook 
  
Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.
  
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
  
> [in] Строка, имена класс сообщения, в которой необходимо разрешить.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как устранена класс сообщения. Можно задать следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Следует разрешить только класс строки сообщения, которые являются точное совпадение.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержащую сообщение, в которой необходимо разрешить. Параметр _pFolderFocus_ может быть NULL. 
    
 _ppResult_
  
> [out] Указатель на указатель на объект сведения возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданной в параметре _szMsgClass_ не соответствует класс сообщения для формы в библиотеке форм. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormMgr::ResolveMessageClass** для разрешения класс сообщения в его формы в контейнере формы. Объекта формы сведения, возвращаемые в параметре _ppResult_ дальнейшей предоставляет доступ к свойствам формы, имеющей класса данного сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы устранить класс сообщения в форму, форма просмотра передает имя класса сообщения разрешения, например, " `IPM.HelpDesk.Software`«. Для принудительной разрешение, точное (то есть, чтобы запретить разрешение базового класса класс сообщения, когда точно соответствующие формы сервер недоступен), флаг MAPIFORM_EXACTMATCH может быть передан в параметре _ulFlags_ . Если параметр _pFolderFocus_ имеет значение NULL, процесс разрешения класс сообщения не выполняет поиск контейнера папки. 
  
Порядок поиска контейнеры зависит от реализации поставщика библиотеки форм. Поставщик библиотеки форм по умолчанию выполняется поиск сначала локального контейнер, а затем в контейнере папки передается в папку, контейнер личных форм и, наконец, контейнер организации.
  
Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.
  
Идентификатор класса для класса разрешить сообщение возвращается в составе объекта данные формы. Предполагается, что идентификатор класса существует в библиотеке OLE до того времени, после просмотра формы называется [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) метод или метод [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) просмотра формы не работают. 
  
## <a name="see-also"></a>См. также



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

