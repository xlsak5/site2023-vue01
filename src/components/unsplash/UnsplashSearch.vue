<template>
  <div className="unsplash__search container">
    <h2 className="blind">검색하기</h2>
    <input
      ref="{inputRef}"
      type="search"
      onKeyPress="{onKeyPress}"
      placeholder="이미지를 검색하세요!"
    />
    <button type="submit">검색하기</button>
  </div>
</template>
