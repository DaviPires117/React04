Header.jsx

import React from 'react';
import './Header.css';

class Header extends React.Component {
  render() {
    return (
      <section className="header-section">
        <h1>Meu Título</h1>
        <p>Um parágrafo de introdução.</p>
      </section>
    );
  }
}

export default Header;
Conteudo.jsx

import React, { Component } from 'react';
import './Conteudo.css';

class Conteudo extends Component {
  constructor(props) {
    super(props);
    this.state = {
      read: 0,
      like: 0,
      dislike: 0,
    };
  }

  handleRead = () => {
    this.setState((prevState) => ({ read: prevState.read + 1 }));
  };

  handleLike = () => {
    this.setState((prevState) => ({ like: prevState.like + 1 }));
  };

  handleDislike = () => {
    this.setState((prevState) => ({ dislike: prevState.dislike + 1 }));
  };

  render() {
    const { read, like, dislike } = this.state;

    return (
      <article className="conteudo-article">
        <h2>Meu Artigo</h2>
        <p>Conteúdo do artigo aqui.</p>
        <div>
          <button onClick={this.handleRead}>Lido: {read}</button>
          <button onClick={this.handleLike}>Gostei: {like}</button>
          <button onClick={this.handleDislike}>Não Gostei: {dislike}</button>
        </div>
      </article>
    );
  }
}

export default Conteudo;
Footer.jsx:
jsx
Copy code
import React from 'react';
import './Footer.css';

class Footer extends React.Component {
  render() {
    return (
      <footer className="footer">
        <p>Todos os direitos reservados &copy; 2023</p>
      </footer>
    );
  }
}

export default Footer;
