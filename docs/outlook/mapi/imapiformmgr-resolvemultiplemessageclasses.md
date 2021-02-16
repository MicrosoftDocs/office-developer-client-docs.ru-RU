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
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428020"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешит группу классов сообщений в их формы в контейнере формы и возвращает массив информационных объектов формы для этих форм.
  
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
  
> [in] Указатель на массив, содержащий имена классов сообщений, которые необходимо разрешить.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет решением классов сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Должны быть разрешены только строки класса сообщений, точно совпадают.
    
MAPIFORM_LOCALONLY
  
> Не включаем кэшные формы.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержаную форму, класс сообщения которой разрешен. Параметр  _pFolderFocus может_ иметь NULL. 
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на массив информационных объектов формы. Если просмотр формы передает NULL в  _параметре pMsgClasses,_ параметр  _ppfrminfoarray_ содержит информационные объекты формы для всех форм в контейнере. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

С помощью метода **IMAPIFormMgr::ResolveMultipleMessageClasses можно вызвать метод IMAPIFormMgr::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений в формы в контейнере формы. Массив информационных объектов формы, возвращаемого  _в ppfrminfoarray,_ обеспечивает дополнительный доступ к каждому свойству формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить группу классов сообщений в формы, просмотр форм передает массив имен классов сообщений для разрешения. Чтобы принудительное разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщений, когда сервер форм, точно совпадающий с другим, недо доступен), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._ 
  
Имена классов сообщений всегда являются строками ANSI, а не Юникодом.
  
Если класс сообщения не может быть разрешен в форму, для этого класса сообщения возвращается NULL в массиве сведений формы. Следовательно, даже если метод возвращает S_OK, просмотр форм не должен работать при предположении, что все классы сообщений успешно разрешены. Вместо этого, просмотры форм должны проверять значения в возвращаемом массиве.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

