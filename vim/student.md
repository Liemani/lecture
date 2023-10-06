vim.md



# index

- vim 의 장점
- 새로운 vim 기능을 어떻게 발견할까?
- simple key
- .vimrc의 다양한 설정
- register: 키마다 존재한다
- 반복 수행
- 추가로 기능 설명



# vim 의 장점
- 가벼워 보인다 (실제 가벼운지는 모름)
- 배터리를 덜 잡아먹을 것 같다 (실제 덜 잡아 먹는지는 모름)
- cli 친화적: cli를 잘 가꾸었다면 vim과의 시너지를 기대할 수 있다



# 새로운 vim 기능을 어떻게 발견할까?

- 인터넷 검색
- help 페이지



# simple key
> 이동을 위한 다양한 키들을 익혀두는 것이 가장 중요하다 (기동성 확보)

```txt
gg
k  {  H  zb  <C-Y>  <C-U>  <C-B>
M  %  f  t  F  T  ,  ;  0  $
j  }  L  zt  <C-E>  <C-D>  <C-F>
G
''  <C-I>  <C-O>
```



# .vimrc의 다양한 설정
- set {option}?
- set {option}
- set no{option}
- set {option}!
- 유용한 option들
    - number
    - color desert
    - syntax on
    - ruler
    - showcmd
    - hlsearch
- keymap
    - nnoremap <Fn> :~<CR>
    - inoremap
    - vnoremap



# register: 키마다 존재한다

- 특수한 용도의 register는 기억해두면 좋다.(`*`, ", 0, /)
- `*`: clipboard와 연동, ssh에서는 연동되지 않는다.
- ": 최근 삭제, 복사한 내용이 자동 저장된다.
- 0: 최근 복사한 내용이 저장한다.
- /: 최근 검색한 내용을 저장한다.
- 특정 register에 문자열을 복사하고 싶은 경우 `"<key>y` 를 하면 된다.
- 특정 register에 저장된 문자열을 붙여넣고 싶은 경우 `"<key>p` 를 하면 된다.
- insert mode에서는 `<C-R><key>` 로 해당 register에 저장된 문자열을 빠르게 붙여넣을 수 있다.



# 반복 수행
> s//

- 고급 sed
    :s/\(\)/\1
- macro: q{key}{macro behavior}q, @{key}
- cgn: highlight 후 highlight 된 부분만 치환, '.'으로 반복
- norm: visual mode로 선택한 각 line을 반복 실행



# 추가로 기능 설명

- fold
- :buffers
- :bufdo
- window
- tab
- mark
